[![GitHub issues](https://img.shields.io/github/issues/jhan15/facial_emotion_recognition)](https://github.com/jhan15/facial_emotion_recognition/issues)
![GitHub last commit](https://img.shields.io/github/last-commit/jhan15/facial_emotion_recognition?color=ff69b4)

# facial_emotion_recognition
Recognize the facial emotions in 7 categories: angry, disgust, fear, happy, sad, surprise, neutral.

## Dataset
The dataset is provided by a competition, which is quite similar to FER2013 dataset.

![image](https://user-images.githubusercontent.com/62132206/122206330-89176380-cea1-11eb-9ef4-01bf1ce95a7c.png)

The training data distribution is shown below.

![image](https://user-images.githubusercontent.com/62132206/122207240-35f1e080-cea2-11eb-8e03-bacda4bfc640.png)

## Model
The API for face detection is Google's [mediapipe API](https://github.com/google/mediapipe). The model for emotion recognition is a 15-layer (8 convs + 4 pooling + 3 fcs) VGG style network.

```bash
Pipeline
├── face detection: mediapipe
└── emotion recognition: vggnet
```
#### VGG architecture
![image](https://user-images.githubusercontent.com/62132206/122204954-004bf800-cea0-11eb-981b-c7b1cbb935fc.png)

#### Data flow

![image](https://user-images.githubusercontent.com/62132206/122206734-dd224800-cea1-11eb-9670-19b718667bbd.png)

#### Upsampling
The upsampling technique is SMOTE.

![image](https://user-images.githubusercontent.com/62132206/122207118-10fd6d80-cea2-11eb-98b1-b13e678be8f7.png)


## Usage
You can try my codes in colab if you are interested in.

#### Train
If you have an dataset, you can train use train.ipynb [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhan15/facial_emotion_recognition/blob/master/training.ipynb)

#### Inference
If you want infer directly, use inference.ipynb [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhan15/facial_emotion_recognition/blob/master/inference.ipynb)

The weights I trained is located in [saved_models](https://github.com/jhan15/facial_emotion_recognition/tree/master/saved_models).

## Result
