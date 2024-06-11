
# 유방암 영상처리 프로젝트

## 프로젝트 개요

### 1. 프로젝트 배경 및 목적
 이 프로젝트는 유방 초음파 이미지를 분석하여 정상, 양성, 악성 종양을 분류하는 모델을 개발하는 것을 목표로 합니다. 
 초음파는 유방암 진단에 널리 사용되는 비침습적 검사 방법으로, 방사선 노출 없이 실시간으로 조직의 상태를 확인할 수 있습니다.

### 2. 데이터셋 소개
데이터 출처: [Kaggle - Breast Ultrasound Images Dataset](https://www.kaggle.com/datasets/aryashah2k/breast-ultrasound-images-dataset)

#### 데이터
- **수집된 데이터**: 25~75세 여성의 유방 초음파 이미지 (2018년에 수집된 자료)
- **환자 수**: 600명
- **이미지 수**: 780개 (평균 이미지 크기: 500x500 픽셀)
- **클래스 분류**: normal, benign, malignant
![](train_data_loader(이미지 시각화).png)

### 3. 필요 라이브러리 & 프로그램
- Python 3.x
- TensorFlow
- Keras
- NumPy
- Pandas
- OpenCV
- Scikit-Learn
- Matplotlib

## 모델 설명
Swin Transformer : 비전 트랜스포머 모델로, 이미지 패치를 계층적으로 처리하여 계산 효율성을 높이고 다양한 비전 작업에서 높은 성능을 발휘
InceptionV3 : GoogLeNet의 발전된 버전으로, 다양한 크기의 필터를 병렬로 적용하여 네트워크 깊이를 효과적으로 증가시키고 계산 비용을 줄
EfficientNet : 모델 크기(너비, 깊이, 해상도)를 균형 있게 확장하는 원칙을 적용하여, 높은 성능을 유지하면서도 효율적인 계산 자원 사용을 목표
ResNet : 잔차 학습(residual learning) 개념을 도입하여 매우 깊은 네트워크에서도 기울기 소실 문제를 해결하고, 뛰어난 성능을 보이는 모델
DenseNet : 각 층이 모든 이전 층의 출력과 연결되어 정보 흐름을 극대화하고, 기울기 소실 문제를 완화하여 효율적인 특성 재사용을 가능하게 함

## 실험 결과
learning rate=0.001
optimizer = Adam
epochs = 50
batch-size = 16

| 모델 | Test Accuracy | Test Loss |
|------|-------|--------|
| vit | 0.5785  | 0.9090 |
| ResNet | 0.7934 | 0.6335 |
| EfficientNet | 0.7769 | 0.9798 |
| DenseNet | 0.8099 | 0.6052 |
| InceptionV3 |  0.8347 | 0.4708 |
| Swin Transformer | 0.6198 | 0.9027 |

## 추후 개선 사항 & 한계점
의료 데이터이다 보니 더 많은 데이터를 수집하는데 어려움이 있어서 아쉬웠다.

