# DisasterAnalysisProject
This project extends the work in [this paper](https://mimran.me/papers/Damage_assessment_from_Social_Media_Images.pdf). That paper uses Machine Learning with convolutional neural networks to try to classify images of disasters have having no, mild, or severe damage from 5 datasets - google data, data from the Ecuador and Nepal earthquakes, and data from Typhoon Ruby and Hurricane Matthew. This project extends that, answering 4 questions:
1. Would batch normalization increase efficacy? The original paper doesn't use it, but would it help.

This project found that batch normalization helps with data from google and the earthquakes, but is worse for the others. However, as a whole, it performs better.

2. Is it more effective to train in order or together for training on multiple datasets? The original paper a few times trained on multiple datasets, like google and both earthquakes. They did it together, by mixing the datasets while training. I was wondering if the opposite woud work as well, where you train in order from google, to the othe earthquake, for example, then to the earthquake it's tested in.

This project found that training together is much more effective.

3. Is it effective to train with google and a similar disaster, then train on a different disaster? The original paper trained on google, then tested on a disaster, and trained on a related disaster (like, another earthquake) then tested on a disaster, but never combined google and a related disaster.

This project found that it is effective, and has fairly high performance.

4. How much additional information from the diaster in questin is needed to perform well, when information is available from google and a related disaster, and is it better to pretrain, then fine tune, or mix the new info in and train from scratch?

This project found that not much data is needed, just 100 images to get decent performance, and that pre-training then finetuning works just fine, which is good as it reduces the amount of time needed.

The full document analyzing this can be found [here](https://docs.google.com/document/d/1hs6zRE0S7NhGgesi-6oHmKgMUE9TFvFd-o7zF6TX9ho/edit?usp=sharing).

The data can be found [here](https://crisisnlp.qcri.org/) under resource number 9.
