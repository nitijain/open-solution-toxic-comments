# Starter code: Kaggle [Toxic Comment Classification Challenge](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge 'Kaggle competition')

Here, at [Neptune](https://neptune.ml/ 'machine learning lab') we enjoy participating in the Kaggle competitions. [Toxic Comment Classification Challenge](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge 'Kaggle competition') is especially interesting because it touches important issue of online harassment.

## The idea
We are contributing starter code that is easy to use and extend. We did it before with [Cdiscount’s Image Classification Challenge](https://github.com/deepsense-ai/cdiscount-starter) and we believe that it is correct way to open data science to the wider community and encourage more people to participate in Challenges. This starter is ready-to-use end-to-end solution. Since all computations are organized in separate steps, it is also easy to extend. Check [devbook.ipynb](https://github.com/neptune-ml/kaggle-toxic-starter/blob/master/devbook.ipynb) for more information about different pipelines.

Now we want to go one step further and invite you to participate in the development of this analysis pipeline. At the later stage of the competition (early February) we will invite top contributors to join our team on Kaggle.

## Contributing
You are welcome to extend this pipeline and contribute your own models or procedures. Please refer to the [CONTRIBUTING](https://github.com/neptune-ml/kaggle-toxic-starter/blob/master/CONTRIBUTING.md) for more details.

# Installation
### option 1: Neptune cloud (fastest)
[Neptune cloud](https://neptune.ml/ 'machine learning lab') is the easiest way to start experimenting. Environment is already prepared, hence you care only about experiments.
1. clone this repo
```bash
$ git clone https://github.com/neptune-ml/kaggle-toxic-starter.git
```
2. register on the [neptune site](https://neptune.ml/ 'machine learning lab') to receive $100 in GPU time.
3. install neptune-cli
```bash
$ pip3 install neptune-cli
```
4. log in to [neptune cloud](https://neptune.ml/ 'machine learning lab') via command line
```bash
$ neptune login

5. Create new project named `toxic` it will generate project-key TOX for you

6. run first experiment
```bash
$ neptune send experiment_manager.py --environment keras-2.0-gpu-py3 --worker gcp-gpu-medium --config neptune_config.yaml -- train_evaluate_predict_pipeline --pipeline_name glove_lstm
```
Now you can observe the progress of your experiment on Neptune dashboard. When its done, you can collect output from the _Browse Files_ (left bar in the Neptune dashboard).

Check [Neptune documentation](https://docs.neptune.ml/cli/neptune_send/) for more options and our [Wiki](https://github.com/neptune-ml/kaggle-toxic-starter/wiki) for detailed explanation of this starter code.

**Happy Training :)**

### option 2: local install
This project assumes python 3.5.
1. clone this repo
```bash
$ git clone https://github.com/neptune-ml/kaggle-toxic-starter.git
```
2. install TensorFlow and Keras.
    - in case you **have GPU**
    ```bash
    $ pip3 install tensorflow-gpu==1.1.0
    $ pip3 install Keras==2.0.8
    ```
    - in case you **do not have GPU**
    ```bash
    $ pip3 install tensorflow==1.1.0
    $ pip3 install Keras==2.0.8
    ```
3. install remaining requirements
```bash
$ pip3 install -r requirements.txt
```
4. register on the [neptune site](https://neptune.ml/ 'machine learning lab') to receive $100 in GPU time.
5. log in to [neptune](https://neptune.ml/ 'machine learning lab') via command line
```bash
$ neptune login

6. Create new project named `toxic` it will generate project-key TOX for you
```
7. run first experiment
```bash
$ neptune run experiment_manager.py -- train_evaluate_predict_pipeline --pipeline_name glove_lstm
```

# Solution visualization
Below end-to-end pipeline is visualized. You can run exactly this one!
![pipeline_001](https://github.com/neptune-ml/kaggle-toxic-starter/blob/master/imgs/log_reg_ensemble.png 'complex-ensemble')

We have also prepared something simpler to just get you started:

![pipeline_002](https://github.com/neptune-ml/kaggle-toxic-starter/blob/master/imgs/glove_lstm_pipeline.png 'simple GLOVE LSTM')


# User support
There are several ways to seek help:
1. Read project's [Wiki](https://github.com/neptune-ml/kaggle-toxic-starter/wiki), where we publish descriptions about the code, pipelines and neptune.
2. Kaggle [discussion](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/discussion) is our primary way of communication.
3. You can submit an [issue](https://github.com/neptune-ml/kaggle-toxic-starter/issues) directly in this repo.
