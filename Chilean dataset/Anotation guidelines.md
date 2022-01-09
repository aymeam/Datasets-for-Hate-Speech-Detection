# Análisis de tweets

Basado en: _Instrumento para evaluar la deliberación, incivilidad y postura (stance) frente a comentarios de usuarios
respecto a noticias publicadas en la página de Facebook de Bío Bío Chile_

```
Libro de códigos
Autora : Magdalena Saldaña
Asistente de investigación : Valentina Proust
```
## INSTRUCCIONES GENERALES

*Las categorías 3 - 8 son nuevas e intentan cubrir el vacío que deja la eliminación de “Tema”. Estas no son
excluyentes y pueden estar presentes al mismo tiempo, por lo que podría haber casos en los que se marquen
todas al mismo tiempo (menos “Otros”, que solo se marcará si no se codificó ninguna de las anteriores).

**1. IDENTIFICACIÓN DEL USUARIO: ANÓNIMO**
    0. Identificado (no anónimo): formato nombre/sobrenombre + apellido.
       Si utiliza nombre corto/apodo en vez del nombre (Marce en vez de
       Marcel@) pero incluye apellido, no se considera anónimo.
    1. Anónimo: cualquier expresión que no sea formato
       nombre/sobrenombre + apellido (ej. Solo sobrenombre, nombres solo
       el nombre (Mario A), o solo el apellido, o repite el nombre (ej: fran
       fran) o sólo incluye los apellidos (Aguirre Astudillo), o escribe nombres
       de superhéroes o personajes de ficción como Superman45 o William
       Wallace, codificar 1.
**2. IDENTIFICACIÓN DEL USUARIO: GÉNERO**
    Se identifica respecto al nombre del usuario (no se revisa el perfil). Si el nombre de
    usuario no permite identificar el género (por ejemplo: usa un pseudónimo), entonces
    se codifica como Indeterminado
       1. **Hombre**
       2. **Mujer**
       3. **Indeterminado**

```
Por ahora, continuaremos considerando en esta variable la intención del usuario respecto al
género. Por ejemplo, Don Segua o Superman calificarían como 1 (Hombre), aun no siendo
nombres reales, porque denotan la intención de identificarse con un género. OJO con los
nombres de empresas o medios de comunicación. Estos deben ser marcados como
indeterminado (aunque lleven pronombres de género, como “El Construidor”)
```
```
En el caso de nombres extranjeros (por ejemplo Shi-Long Loi, o Drangaft Neriamang), se
codificará 3 (Indeterminado) en aquellos casos donde no se deduzca el género de la persona.
No se deberá buscar en internet un nombre que no se conoce.
```

**3. Mención migración**
    Si el tweet alude de manera directa o indirecta a la inmigración/migrantes en Chile,
    marcar 1, de lo contrario marcar 0. Ej.: “@AgriculturaFM La bancada @PDC_Chile que
    se lleve a su sede a los venezolanos que entraron ilegalmente y que tienen
    antecedentes penales y por supuesto que los alimenten ya que están tan
    preocupados.”
    Para las menciones, con que aparezca un concepto relacionado con la variable, se
    considerará como que está presente. No es necesario que lleve una valoración.
    **OJO** : si se menciona la nacionalidad de una persona, pero no hay un contexto que
    aluda a la migración (ej.: “Boliviano ql”), NO se debe marcar.
**4. Mención Venezuela**
    Si el tweet alude a la situación política de Venezuela, Maduro, Chávez, etc., marcar 1,
    de lo contrario marcar 0.
    **OJO** : si se mencionan migrantes de nacionalidad venezolana, NO se debe marcar
    (corresponde a “mención migración”)
    Para las menciones, con que aparezca un concepto relacionado con la variable, se
    considerará como que está presente. No es necesario que lleve una valoración.
**5. Mención política nacional**
    Si el tweet alude a figuras del mundo de la política, campañas, candidatos, partidos
    políticos u otras dimensiones relacionadas con la política nacional, marcar 1, de lo
    contrario marcar 0. La mención debe ser explícita a un sujeto/evento/partido político.
    NO se considerará mención política nacional si se habla de la izquierda, la derecha o
    comunistas (a menos que se habla explícitamente del PC o alguno de sus miembros).
    SÍ se marca mención política si es que se habla de oposición/oficialismo.

```
Para las menciones, con que aparezca un concepto relacionado con la variable, se
considerará como que está presente. No es necesario que lleve una valoración.
*Aunque se mencione a una figura política fuera de su contexto político (ej. Hablar de
la vida privada de un candidato), sí se debe marcar “mención política nacional” (por lo
tanto, incorpora parte de lo que era el antiguo tema 34. Celebridad).
OJO : si se menciona solo política internacional, no se debe marcar (se debe marcar
solo cuando el tweet alude en alguna parte a elementos de la política nacional).
```
**6. Mención grupos marginalizados**
    Por grupos marginalizados vamos a entender exclusivamente: mujeres y disidencias
    sexuales y de género.
    Si el tweet alude a alguno de estos grupos (ej. las causas feministas, orgullo gay,
    transexuales, etc.), marcar 1, de lo contrario marcar 0.
    Para las menciones, con que aparezca un concepto relacionado con la variable, se
    considerará como que está presente. Sin embargo, el concepto debe estar en un
    contexto que denote claramente la marginalización del grupo (ej. No sirve “Machi


```
Francisca Linconao, una mujer que lucha por su pueblo Mapuche” pero sí algo como
“Machi Francisca Linconao, una mujer que lucha por las mujeres maltratadas del
pueblo Mapuche”.
```
**7. Mención “Otros”**
    Si el tweet alude temas que NO son migración, Venezuela, política nacional o grupos
    marginalizados, marcar 1. De lo contrario, marcar 0 (en consecuencia, **si ya se marcó**
    **1 en alguna de las 4 categorías anteriores, necesariamente acá tienen que marcar 0** ).

```
Acá entran especialmente esos tweets que no tenían una temática clara (ej.:
“Boliviano ql”) o que hablan de temas que no forman parte de las primeras 4
categorías (ej. Football, economía, etc).
```
**8. USO DE MAYÚSCULAS**
    Si el tweet o parte del tweet está escrito con mayúsculas, codificar 1. De lo contrario,
    0 (se excluyen las siglas que de por sí se escriben con mayúscula, como FBI, NASA,
    UDI, etc.).
**9. GROSERÍA/LENGUAJE VULGAR CON INTENCIÓN**
    Si el tweet contiene grosería y/o lenguaje vulgar que tiene un claro objetivo de
    insultar a otra persona, independiente si es hacia otro comentarista u otra persona (o
    grupo de personas, como un partido político), codificar 1. De lo contrario, 0. No se
    cuenta el número de grosería, sino presencia/ausencia de éstas. Ejemplos:
    “A tu hermana le meten varios goles por semana” (lenguaje vulgar)
       “Esa Bachelet es una yeta de mierda” (grosería)

En el caso de “weón”, se considerará que tiene intención cuando funciona como un adjetivo
(ej. él es muy aweonado) o cuando es un **sustantivo que va acompañado por otro adjetivo
peyorativo** (ej. el weon tonto; el weón chamullento).

Caso CTM (y similares): se debe estar aludiendo de manera directa a un sujeto (humano, no
objeto ni animal ni lugar). Ej. “El CTM ese...”. Si no alude a un sujeto, se interpretará que es
un exclamación del estado de ánimo del hablante y, por lo tanto, es grosería sin intensión.

Caso “culiao”: todos sus usos son considerados como grosería con intención (no importa qué
tan “amistoso” sea el trato).

Para considerar que la grosería carga con intención, tiene que estar directamente aludiendo
a una persona, grupos de personas o instituciones/países (se entiende que se está aludiendo
a las personas que forman parte de estas agrupaciones). Si la grosería va en contra de un
objeto, lugar (ej. Santiago ql), animal, etc., NO se considera. Si no es posible identificar que la
grosería está siendo dirigida a alguien en concreto, NO se considera (ej. Cuando es un CTM al
final de una oración, demostrando la ira/emoción de una persona).


## 10. GROSERÍA/LENGUAJE VULGAR SIN INTENCIÓN

```
Si el tweet contiene grosería y/o lenguaje vulgar que está presente pero que no tiene
como un fin claro el de insultar a otra persona (o grupo de personas), codificar 1. De
lo contrario, 0. No se cuenta el número de grosería, sino presencia/ausencia de éstas.
Ejemplos:
“¿Qué mierda esta situación?”
“Estos políticos juran que somos weones”
```
El uso de “weón” no se tomará como con intensión en aquellos casos en que funcione como
sustantivo sinónimo de “persona/ser humano” y, por lo tanto, pueda ser reemplazado por
este (ej. llegué tarde porque había muchos weones en la fila del cajero = me demoré mucho
porque había muchas personas en la fila del cajero). También se consideran como sin
intensión los casos en que se usa como una muletilla de cierre de oración (ej. estuvo cuatica
la junta wn).

Para considerar que la grosería no carga con intención, no se tiene que estar directamente
aludiendo a una persona, grupos de personas o instituciones/países. Si la grosería va en
contra de un objeto, lugar (ej. Santiago ql), animal, etc., tampoco se considera.
Si no es posible identificar que la grosería está siendo dirigida a alguien en concreto, es
altamente probable que sea parte de la expresión exacerbada de emoción de una persona,
por lo que se considera que no carga con intención (ej. Gooooooooooooooooool ctm).

## 11. INSULTO/SOBRENOMBRE

```
Si el tweet incluye sobrenombres, frases, o palabras ofensivas que no son
groserías, codificar 1. De lo contrario, 0. Ejemplo:
“Ahí se nota tu falta de cerebro”
“Y qué dijo Chanchelet?”
“Eres un imbécil”
```
```
OJO : debe estar de manera clara el insulto/sobrenombre en el tweet. NO sirve
interpretar el tweet completo como algo insultante.
```
```
Se consideran como insultos el tratar a alguien de machista o feminista
Se considera como estereotipo E insulto el uso de la expresión “seres de luz” para
hacer referencia a la comunidad haitiana en Chile.
```
```
“tener el culo asegurado”: insulto
Delincuente: insulto
```

## 12. ESTEREOTIPO

```
Si el tweet incluye frases o estereotipos que denigran a un grupo (como mujeres,
inmigrantes, minorías raciales, minorías sexuales), codificar 1. De lo contrario, 0.
Ejemplo:
“A tu mujer hay que agrandarle la cocina para que esté contenta”
“Cuidado que es mapuche – no te vaya a quemar la casa”
“No esperaba menos de una comunista en todo caso. Lo raro sería que propusiera
trabajar más”
```
```
* Si es que el tweet inicial del hilo menciona un estereotipo y el tweet que estamos
analizando entrega un ejemplo/caso particular que respalda ese estereotipo, se
marcará 1 (recuerden el ejemplo de los argentinos en Europa).
```
A raíz de la naturaleza del caso de estudio, esta variable incluirá expresiones estereotípicas
de la clase política en general (Ej: “políticos corruptos”, “políticos ladrones”), así como
estereotipos relacionados a la izquierda (Ej: “zurdos flojos”, “se la pasan pidiendo
subvenciones”), o relacionados a la derecha (Ej: “fachos ladrones”, “apitutando a todos los
primos”) etc.

**En conclusión... SOLO marcaremos estereotipos cuando se esté denigrando a uno de los
siguientes grupos:**

**- Mujeres (ej. Las feministas, el feminismo...)
- Inmigrantes
- Minorías raciales/indígena (ej. Mapuches)
- Minorías sexuales
- Políticos (de cualquier lado) *asociación de características de un sector a una persona o
grupo de personas. El “pueblo” sí tiene un carácter político. Ejemplos de estereotipos
políticos (ej. Políticos corruptos/ladrones/ineptos/privilegiados/payasos/etc...). Si es el
político + una groseria, tiene que quedar claro a qué apunta (ej. “el político csm” no sirve,
pero si “los políticos csm ladrones”)**

**Recuerden que la identificación del estereotipo sigue la estructura “grupo estereotipado” +
“característica negativa” (ej. Comunistas flojos, fachos autoritarios).
Las excepciones serían conceptos como “feminazi” que ya cargan con la valoración
negativa.**


## 13. HUMOR (IRONÍA, BURLA, SARCASMO, SENTIDO FIGURADO)

```
*Vamos a asumir lo mejor de la gente y que no están diciendo brutalidades que
creen ciertas en Twitter, sino que pueden estar cargando con
humor/sarcasmo/ironía.
El contexto de la cadena (y todos los elementos que vengan en el tweet analizado)
pueden ser usados como argumentos para justificar la presencia de alguno de los
tipos de humor.
```
```
Si el tweet incluye palabras o expresiones que se entiendan como irónicas**,
expresiones burlescas o sarcásticas, o representaciones de la risa (ej. jajaja, XD,
jijiji, etc.), ya sea referidas a otro usuario o hacia la noticia, codificar 1. De lo
contrario, 0. Dentro de las representaciones de la risa se consideran los emojis (ej.
🤣 😂 😆). Ojo, el emoji debe ir acompañado por un texto, no puede ser el
único contenido del tweet.
Es importante que la presencia del humor sea explícita, y no pueda ser confundida
como algo dicho de manera seria.
No importa si el tweet además de ser burlesco, se lee como ofensivo (insulto) o no,
no importa si ya se codificó como insulto (NO SON EXCLUYENTES).
```
```
Ejemplo ironía:
“Ohh!!! Que buena mi presidenta, que gran ejemplo para la region, que gran
mandato ha hecho, weeennaaa!!! Se passooo! Con todo esto, todavia no entiendo
porque el Presidente Trump NO la recibio en la Casa Blanca, fue la unica
mandataria de la region a la que le cerraron la puerta, Porque?????”
```
```
Ejemplo burla:
“jajaja, maricón con cola”
```
```
Otro ejemplo:
Una adivinanza: "Blanco es su pelo, roja es su parka, que devuelva la plata del
Banco de Talca" quien esssss??
```
```
**Según la Real Academia Española (RAE), ironía es “Expresión que da a entender
algo contrario o diferente de lo que se dice, generalmente como burla disimulada”
```
```
Se considerará como burla el tratar a alguien de “bot”
```

## 14. PLANTEA PREGUNTA LEGÍTIMA

```
Si el tweet plantea preguntas que no son retóricas (“¿Por qué eres tan ridículo”)
sino que invitan a la deliberación (“¿me puedes explicar qué significa este
número?” “¿tienes más información?” “¿Te parece correcto que el ministro dijera
xx?”, codificar 1. De lo contrario, 0.
```
```
Tweets en los que se piden recomendaciones (¿qué película podría ver en
Netflix? ¿por quién debería votar el domingo?) no se consideran pregunta
legítima.
Pueden considerarse preguntas legítimas preguntas dirigidas a una persona en
específico, la esté arrobando o no.
```
```
“Qué opinan?...” da cuenta de intención de deliberar (a menos que venga
acompañado de un insulto o que se “de la respuesta” inmediatamente)
```
## 15. PROVEE EVIDENCIA

```
Si el tweet provee evidencia (numérica/estadística, o cita estudios, o entrega links
con más información), codificar 1. De lo contrario, 0.
```
```
Se considera evidencia tanto links que lleven a una pagina fuera de Twitter como a
otros tweets. Lo importante es que se esté entregando información que
respalde/justifique el argumento o idea que entrega el usuario.
```
**16. MENCIÓN FIGURA FEMENINA EN TWEET**
    Si el tweet menciona a una mujer (aunque dicha mujer no sea protagonista),
    codificar 1. De lo contrario, codificar 0.
    No se consideran como menciones a figura femenina los arrobas a usuarios que
    no forman parte del tweet o no están relacionados con ella. Sí se deben
    considerar cuando es posible relacionarlos con el contenido del comentario (ej. se
    etiqueta a Paula Daza en un tweet relacionado con el COVID)

## 17. MENCIÓN FIGURA MASCULINA EN TWEET

```
Si el tweet menciona a un hombre (aunque dicho hombre no sea protagonista),
codificar 1. De lo contrario, codificar 0.
No se consideran como menciones a figura masculina los arrobas a usuarios que
no forman parte del tweet o no están relacionados con ella. Sí se deben
considerar cuando es posible relacionarlos con el contenido del comentario (ej. se
etiqueta al ministro Paris en un tweet relacionado con el COVID)
La lógica de esta variable es la misma que la anterior (mención figura femenina en
tweet).
```