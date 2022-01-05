
## Comparative Framework
In the related literature of hate speech detection, there is a lack of comparative studies. 
This situation is more noticeable in cross-lingual approaches as a relatively new sub-area.
There is no consensus about the best approaches for solving the cross-lingual detection task. 

With the purpose of alleviating this situation, we propose two tools for cross-lingual approaches comparison:
1. A python library that contains published cross-lingual hate speech detection models as methods: The library has five published models. 
    Each model consists of the original implementation code as a sub-module, plus a class interface that standardizes all models' input to simplify their use. 

    In addition, the library contains the main class whose attributes are the previously mentioned models and auxiliary tools for evaluation and data management. [Framework for hate speech detection](https://github.com/aymeam/hate-speech-framework)


2. An open competition in [Codalab](https://codalab.org/) for further comparison. We set up an open competition in Codalab to promote fair comparison among cross-lingual approaches. Different leaderboards can be found for three different datasets.
 
