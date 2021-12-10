1. semiconductorzip, semiconductor.z01 파일 다운후 C드라이브에 압축풀기

2. cmd 입력창에 명령어 입력

   1) 경로 변경 : cd C://yolov5
   2) 필요 라이브러리 설치 : pip install -r requirements.txt
   3) 스크립트 파일 실행 : python detect.py
   4) 반도체 이미지 결함 탐지결과 저장 저장 경로: C://yolov5/runs/detect/result

*** cmd에서 실행이 안 되는 경우

anaconda 설치 후 anaconda prompt에서 사용방법 1-3까지 실행
CUDA 관련 오류
https://developer.nvidia.com/cuda-toolkit-archive 에서 CUDA 최신 버전 다운로드
내컴퓨터 - 우클륵 속성 - 고급 시스템 설정 - 고급 - 환경변수로 이동
시스템 변수에 Path 편집
아래 두 줄 입력 후 재부팅 C:\Progran Files\NVIDIA GPU Computing Toolkit\CUDA\v11.4\bin C:\Progran Files\NVIDIA GPU Computing Toolkit\CUDA\v11.4\libnvvp
cmd 실행
pip install tensorflow 입력해서 tensorflow 설치
