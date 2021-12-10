![header](https://capsule-render.vercel.app/api?type=waving&color=random&text=반도체_불량검출&animation=fadeIn&fontColor=B5B5B6)

<h5 align='center'> Using Tech </h5>

<p align='center'>
  <img src="https://img.shields.io/badge/Python-3766AB?style=flat-square&logo=Python&logoColor=white"/></a>&nbsp
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=Jupyter&logoColor=white"/></a>&nbsp
  <img src="https://img.shields.io/badge/Colab-F9AB00?style=flat-square&logo=Google Colab&logoColor=white"/></a>&nbsp
  <img src="https://img.shields.io/badge/Numpy-013243?style=flat-square&logo=Numpy&logoColor=white"/></a>&nbsp
</p>



##### [김진](https://github.com/rumcrush)
![](https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=rumcrush&theme=monokai)

##### [박민아](https://github.com/parkmina365)
![](https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=parkmina365&theme=monokai)


#### 2021.11.15(월) Start

# Semiconductor defect inspection

#불량 반도체 탐지 결과
<img scr="https://imgur.com/70NbjpA">

#설명 
반도체 이미지를 활용하여 YOLOv5 딥러닝 이미지 객체탐지 모델을 활용하여 불량품 반도체를 탐지하는 프로그램입니다. 결함 예측률을 통하여 양품, 불량품 반도체를 탐지하고 결과이미지를 별도로 저장합니다.

# 프로젝트 절차 
## 1. 이미지 탐색
OpenCV 모듈을 사용하여 전처리에 사용할 이미지를 선정했습니다.

## 2. 이미지 전처리
이미지 상으로 보이는 반도체 결함을 점, 선, 크기별로 어노테이션을 만들어 바운딩박스 처리합니다. 

## 3. 모델링
Detectron2, YOLO R, mobileNetSSDv2, YOLOv5로 반도체 불량품 탐지에 가장 적합한 모델을 테스트 했습니다.
그 중 YOLOv5가 가장 뛰어난 학습 결과를 보였으며
클래스별 mAP 측정 결과 최대 0.995를 도출 했습니다.

## 4. 파이썬 스크립트파일 구축 
모델링 파이썬 스크립트 파일로 만들어 로컬 환경(windows, mac)에서도 구동 될 수 있도록 프로그램을 구축 했습니다.
결과물은 semiconductor.zip 파일을 다운로드 받아주세요.

#### 사용 방법 
1. semiconductor.zip 파일 다운후 C드라이브에 압축풀기

2. cmd 입력창에 명령어 입력
 	1) 경로 변경 : cd C://yolov5
 	2) 필요 라이브러리 설치 : pip install -r requirements.txt
 	3) 스크립트 파일 실행 : python detect.py 

3. 반도체 이미지 결함 탐지결과 저장
저장 경로: C://yolov5/runs/detect/result

** cmd에서 실행이 안 되는 경우 
1. anaconda 설치 후 anaconda prompt에서 사용방법 1-3까지 실행 
2. CUDA 관련 오류
  1) https://developer.nvidia.com/cuda-toolkit-archive 에서 CUDA 최신 버전 다운로드 
  2) 내컴퓨터 - 우클륵 속성 - 고급 시스템 설정 - 고급 - 환경변수로 이동 
  3) 시스템 변수에 Path 편집 
  4) 아래 두 줄 입력 후 재부팅 
      C:\Progran Files\NVIDIA GPU Computing Toolkit\CUDA\v11.4\bin
      C:\Progran Files\NVIDIA GPU Computing Toolkit\CUDA\v11.4\libnvvp
  5) cmd 실행 
  6) pip install tensorflow 입력해서 tensorflow 설치    
