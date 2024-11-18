# Image Based Real Time Fire Detection and Rescue Target Identification AI System
[📄 Project Poster PDF](https://github.com/yejinyeo/Image-Based-Real-Time-Fire-Detection-and-Rescue-Target-Identification-AI-System/blob/main/poster.pdf) / [📄 Project Report PDF](https://github.com/yejinyeo/Image-Based-Real-Time-Fire-Detection-and-Rescue-Target-Identification-AI-System/blob/main/report.pdf)

## Introduction
본 프로젝트는 YOLO v4를 활용하여 실시간 화재 감지와 구조대상자 파악이 가능한 AI 시스템을 구현한 것입니다. 약 1700여 장의 다양한 화재 이미지를 Roboflow를 통해 수집 및 학습하여, 일상적인 화재부터 재해 상황까지 효과적으로 탐지할 수 있도록 구성했습니다. 이 시스템은 실시간으로 화재를 감지하고, 구조대상자를 식별 및 인원수를 파악하여 신속한 대응과 구조의 편의성을 제공합니다.

#### 주요 기능
- **화재 감지**: 불꽃 및 연기를 실시간으로 탐지
- **구조대상자 파악**: 사람을 탐지하고 인원을 자동으로 계산
- **모델 결합**: 화재 감지와 구조대상자 탐지를 통합한 시스템 구현


## Implementation
#### 화재 감지 모델
- Roboflow를 통해 1,731개의 불꽃 및 연기 이미지를 수집하고 이를 학습 데이터로 사용
- YOLO v4 알고리즘을 기반으로 불꽃과 연기를 탐지하는 AI 모델을 구현
- 학습 시간 최적화와 데이터 증강 기법을 적용하여 모델 성능 개선

#### 구조대상자 파악 모델
- 사전 훈련된 YOLOv4 모델을 활용하여 사람을 탐지하고 인원수를 계산하는 기능 추가
- 다크넷 모듈을 사용하여 객체 탐지 네트워크를 구성

#### 모델 결합
- 화재 감지와 구조대상자 탐지 모델을 통합하여 하나의 시스템으로 구현
- 각 객체(불꽃, 연기, 사람)의 개수를 카운팅하고 화재 여부를 판단하는 조건을 설정


## Results and Performance
- **최종 화재 감지 정확도**:
  - 불꽃 (AP): 75.50%
  - 연기 (AP): 63.95%
- **학습 시간**: 약 1시간 40분 (1,731개의 데이터셋 기준)
- 두 모델을 결합하여 화재 감지 및 구조대상자 파악 결과를 직관적으로 출력 가능함
