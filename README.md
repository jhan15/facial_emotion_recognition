[![GitHub issues](https://img.shields.io/github/issues/jhan15/facial_emotion_recognition)](https://github.com/jhan15/facial_emotion_recognition/issues)
![GitHub last commit](https://img.shields.io/github/last-commit/jhan15/facial_emotion_recognition?color=ff69b4)

# facial_emotion_recognition
Recognize the facial emotions in 7 categories: angry, disgust, fear, happy, sad, surprise, neutral.

## Dataset
The dataset is provided by a competition, which is quite similar to FER2013 dataset. The training data distribution is shown below.

![image](https://user-images.githubusercontent.com/62132206/122206019-32aa2500-cea1-11eb-9986-368dd29ab7da.png)

## Model
The API for face detection is Google's [mediapipe API](https://github.com/google/mediapipe). The model for emotion recognition is a 15-layer (8 convs + 4 pooling + 3 fcs) VGG style network.

```bash
Pipeline
├── face detection: mediapipe
└── emotion recognition: vggnet
```
### VGG architecture
![image](https://user-images.githubusercontent.com/62132206/122204954-004bf800-cea0-11eb-981b-c7b1cbb935fc.png)
