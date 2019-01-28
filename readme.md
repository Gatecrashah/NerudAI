# NerudAI

Machine Learning based "poet".

This solution was built using Pytorch based fastai library. 

More specific model architecture used to create the poems is an ASGD Weight-Dropped Quasi-Recurrent Neural Network that was pre-trained with WikiText-103 dataset and then fine-tuned with a small dataset of Pablo Neruda's poems. It has recurrent structure and a hidden state that is updated everytime it sees a new word. This hidden state thus contains information about the sentence up to that point.

This model was then wrapped into a Starlette.io application framework that is being served through an ASGI server, Uvicorn. The application was then deployed into AWS EC2 instance using Docker and Elastic Beanstalk.
