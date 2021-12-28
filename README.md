# kaggle-chestXray-penumonia
https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia

## 01.문제정의
Gray channel의 chest image를 폐렴질병(pneumonia)을 분류하는 테스크

## 02.데이터
5,863 X-Ray 이미지(JPEG)로 구성된 이진 분류 데이터로 Normal, Pneumonia로 구성

- 학습데이터 
  - 5216 장 (Normal: 1341장, Pneumonia: 3875장)
- 테스트데이터 
  - 624 장 (Normal: 234장, Pneumonia: 390장)
- 데이터 특징
  - Gray chennel의 jpeg 파일
  - Chest Center X-ray 

- 폐렴에 대한 정보 및 이미지적 특성
1. 폐렴에 대한 정보

- 폐렴이란 폐의 염증을 의미하는 것으로 **일반적으로 X-ray 영상에서 하얀 부분이 강조되서 보인다.** 


- 질환에 의한 폐렴: 세균성 폐렴(Bacterial pneumonia), 바이러스성 폐렴(Viral pneumonia)
그외의 원인으로 인한 폐렴: 자가면역질환, 선천적-유전적 염증
 
2. 질환에 의해 생기는 폐렴의 X-ray 영상에서 보이는 특징

- 세균(박테리아)성 폐렴(Bacterial pnemonia): 마치 침을 '퉤'하고 뱉은 것 처럼 **병변이 폐의 중심 또는 아래쪽에서 하얗게 뭉쳐있는 것이 특징
병변이 중심은 하얀부분이 강하게 뭉쳐져 Consolidate의 형태를 보이지만 외곽부로 가면 불규칙하게 반투명한 부분**(GGO: Ground-glass opacification)이 퍼져나간다.
- 바이러스성 폐렴(Viral pneumonia): **분무기로 뿌린 것처럼 폐의 영역이 전체적으로 희뿌옇게 보인다.**
세균성 폐렴과 반대로 폐 영역 전체적으로 주로 GGO들이 퍼져있으므로 희뿌옇게 보이면 중간중간 작지만 하얗게 뭉쳐진 Consolidate가 보이기도 한다.




## 03. EDA
### 훈련데이터셋 VS 테스트테이터셋
<img src="/static/EDA_train_test_dataset.png" width="30%" height="30%">

### 정상데이터셋 VS 폐렴테이터셋
<img src="/static/EDA_normal_pneumonia_dataset.png" width="30%" height="30%">

### 정상인 CT image 
<img src="/static/Normal CT image.png" width="30%" height="30%">

### 폐렴 CT image 
<img src="/static/Pneumonia CT image.png" width="30%" height="30%">


### 정상인 CT image 히스토그램
<img src="/static/Normal CT image hist.png" width="30%" height="30%">

### 폐렴 CT image 히스토그램
<img src="/static/Pneumonia CT image hist.png" width="30%" height="30%">
이미지 히스토그램을 통해 정상인의 경우 고르게 분포 된 반면에 폐렴환자의 이미지는 100~200 밝기를 가지는 pixel이 모여 있는 것을 알 수 
