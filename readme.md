<div align = "center">


<h2>Shreshth Arora Project</h2>


# ML Library Project

![PythonCI](https://github.com/AroraShreshth/ucs757-project1/workflows/PythonCI/badge.svg)
</div>

## About  💫

The Aim of the project is to provide a holistic website for easy access to ML models via a clean Interface a and options for users
 
Project 1: Emotion Detection System.

### Some Salient Features of Project 🔭
    This project aims to classify the emotion on a person's face into one of seven categories, using deep convolutional neural networks. The model is trained on the FER-2013 dataset which was published on International Conference on Machine Learning (ICML). This dataset consists of 35887 grayscale, 48x48 sized face images with seven emotions - angry, disgusted, fearful, happy, neutral, sad and surprised.


## Getting Started ⚙️

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. 

We follow a systematic Git Workflow -
- Create a fork of this repo.
- Clone your fork of your repo on your pc.
- [Add Upstream to your clone](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/configuring-a-remote-for-a-fork)
- **Every change** that you do, it has to be on a branch. Commits on master would directly be closed.
- Make sure that before you create a new branch for new changes,[syncing with upstream](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/syncing-a-fork) is neccesary.


### Setup and running of project (Backend) 🧮
- Fork the repo and clone it.
- Go in the repo and setup virtual environment using <br>
```python -m virtualenv venv``` 
- Then activate the environment using <br>
    On Windows
```source venv/Scripts/activate```
    On MacOS/Linux
```source venv/bin/actiavte```
- Install requirements\
```pip install -r requirements.txt```

- Change into the `./proj` directory.
   > All the following steps are to be executed in the proj directory.

-- below two are optional steps --
- set secret key for your django project.
- You can use [https://djecrety.ir/] to generate your secret key


- After the above setup, run \
```python manage.py makemigrations```\
```python manage.py migrate```

- Start the backend server\
    ```python manage.py runserver```\
    Runs the backend server at default port ```8000```.\
    Open [http://localhost:8000](http://localhost:8000) to view it in the browser.

The page will reload if you make edits.<br />


#### Note
- If you are adding any new requirements for the project, make sure that you are adding it to ```requirements.txt```


## Built With ⚒
### Backend & Website 📡
* [Django 3.0](https://www.djangoproject.com) - The web framework used in the project.
* [Tensorflow](https://www.tensorflow.com) - Framework used to train and test the models and responses
* [Postgres](https://www.postgresql.org/) - Backend DB used to store final responses from the Tensorflow Emotion Detection Model

  
  
## Versioning 🗓

We use [SemVer](http://semver.org/) for versioning. 

# Using Model Files

- [Download the FER-2013 dataset from here and unzip it inside the src folder.](https://drive.google.com/file/d/1R0PT0bzZEt4mr_EniLRJYmM4vxI_No2p/view?usp=sharing)
This will create the folder data.

- If you want to train this model, use:

```
cd model
python emotions.py --mode train
```

- If you want to view the predictions without training again, you can download the pre-trained model from here and then run:

```
cd model
python display.py
```
- This implementation by default detects emotions on all faces in the webcam feed. With a simple 4-layer CNN, the test accuracy reached 63.2% in 50 epochs.

![Accuracy plot](model/accuracy.png)