# 전자 의료 기록(EHR) 기반 질병 예측 모델의 Source-free Domain Adaptation 적용 및 성능 비교
본 연구는 전자 의료 기록(EHR)을 활용하여 다른 병원으로부터 공유받은 질병 예측 모델을 원본 학습 데이터 없이(source-free) 보유하고 있는 데이터만으로 모델의 예측 성능을 유지할 수 있도록 도메인 적응(Domain Adaptation) 기법 중 TENT(Test-time Entropy Minimization) 알고리즘을 적용하여 그 효과를 비교·분석하는 연구임.


## 연구 배경
### 1. 병원 간 이질적인 데이터
병원마다 질병 및 정상 환자의 데이터 분포, 측정 기기, 진단 기준 등이 서로 달라 데이터의 양상이 이질적이며, 환자들의 진단, 처방, 검사 결과 등의 의료 정보를 전자적으로 기록하는 EHR 데이터 또한 표준화된 형태가 없어 병원마다 형태와 분포가 다름.

### 2. 공유 불가한 원본 학습 데이터
의료 데이터는 개인정보 보호 문제로 인해 병원 간 직접적인 데이터 공유가 어려우며, 원본 학습 데이터를 제외한 AI 모델만 공유가 가능해 모델을 공유받더라도 병원이 보유하고 있는 데이터만 사용할 수 있음.

### 3. 공유된 모델의 낮은 예측 성능
특정 병원에서 원본 학습 데이터 없이(source-free) 학습된 모델만 공유된다는 점, 모델을 공유한 병원(source domain)과 공유 받은 병원(target domain) 간의 데이터 이질성을 원인으로 공유된 모델이 충분한 성능을 발휘하지 못하는 경우가 많음.

 
## 사용 Software source
EHR data - eICU Collaborative Research Database https://eicu-crd.mit.edu/<br/>
TENT Official Github https://github.com/DequanWang/TENT<br/>
Med-BERT https://github.com/ZhiGroup/Med-BERT
