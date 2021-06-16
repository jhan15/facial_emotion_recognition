# facial_emotion_recognition
Recognize the facial emotions in 7 categories: angry, disgust, fear, happy, sad, surprise, neutral.

## Model
The API for face detection is Google's [mediapipe API](https://github.com/google/mediapipe). The model for emotion recognition is a 11-layer VGG style network.

```bash
Pipeline
├── face detection: mediapipe
└── emotion recognition: vggnet
```
### VGG architecture
![image](https://user-images.githubusercontent.com/62132206/122204954-004bf800-cea0-11eb-981b-c7b1cbb935fc.png)
