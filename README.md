# aws

## g5-large 그래픽카드 사양nvidia-smi
### ![image](https://user-images.githubusercontent.com/54635552/178092965-4b788c96-102d-4a52-bd52-db6030a4160c.png)

## 학습 parameter
- --Transformation TPS --FeatureExtraction ResNet --SequenceModeling BiLSTM --Prediction CTC \
- --data_filtering_off --workers 4 --imgH 80 --imgW 400 \
- --num_iter 70000 --valInterval 1000 --batch_size 96
- Star-net 이용 , (H,W) 기존보다큰 80,400으로 진행 , batch_size 96, 총 7만 iter 학습, 1000 iter단위 validation
- 
## 학습 시간 계산
- 1000 iter 45분 소모
- 70000 iter = 70 * 45 = 3150분 = 52.5시간 = 2.2일 소모
- 
