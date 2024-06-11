
# 유방암 영상처리 프로젝트

## I. 프로젝트 개요

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

### 3. 필요 라이브러리 & 프로그램
- Python 3.x
- TensorFlow
- Keras
- NumPy
- Pandas
- OpenCV
- Scikit-Learn
- Matplotlib

## III. 모델 설명
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

## IV. 실험 결과
(여기에 실험 결과를 상세히 기술하세요)

## VI. 추후 개선 사항 & 한계점
(여기에 프로젝트의 한계점과 향후 개선 사항을 기술하세요)
