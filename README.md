# aws

## aws 학습방법
- anaconda 설치
- GPU 버전에 맞는 nvidia 그래픽드라이버와, cuda , torch 설치(버전 호환안되면 GPU 작동안함)
- anaconda 가상환경에서 pip 종속성체크확인하고, 모델학습시작
- 추후에 Docker을 이용하여 좀더 간편한 종속성 문제해결

## Deep-text-recognition(Star-net 학습)
### aws g5-large 그래픽카드 사양 nvidia-smi
### ![image](https://user-images.githubusercontent.com/54635552/178092965-4b788c96-102d-4a52-bd52-db6030a4160c.png)

### 학습 parameter
- --Transformation TPS --FeatureExtraction ResNet --SequenceModeling BiLSTM --Prediction CTC \
- --data_filtering_off --workers 4 --imgH 80 --imgW 400 \
- --num_iter 70000 --valInterval 1000 --batch_size 96
- Star-net 이용 , (H,W) 기존보다큰 80,400으로 진행 , batch_size 96, 총 7만 iter 학습, 1000 iter단위 validation

### 학습 시간 계산
- 1000 iter 45분 소모
- 70000 iter = 70 * 45 = 3150분 = 52.5시간 = 2.2일 소모

### 학습 과정
### ![image](https://user-images.githubusercontent.com/54635552/178093100-2e56a9a8-ecdf-484d-9469-7ab89a9f6259.png)
### log_train.txt 파일
