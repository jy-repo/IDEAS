# vocab

### general
- 성능 지표
  + 정밀도 (precision): True 라고 예측한 값 중 실제 True 인 값의 비율.
  
      precision = TP / (TP + FP)
  
  + 재현율 (recall): 전체 True 중에 모델이 True 라고 예측한 값 비율.
 
      recall = TP / (TP + FN)
      
  + 정확도 (accuracy): 전체 예측 값과 정답 중 옳게 예측한 값 비율.
  
      accuracy = (TP + TN) / (TP + TN + FP + FN)
      
      ※ Object Detection 에선 TN 값 = 0.
  
  + F1 score: precision과 recall의 조화 평균.
  
      F1-score = 2 x (precision x recall) / (precision + recall)
      
  + Fall-out = FPR (False Positive Rate): 실제 False 중 모델이 True 라고 예측한 값 비율.
  
      Fall-out(FPR) = FP / (TN + FP)
      
  + ROC (Receiver Operating Characteristic) curve: Recall-Fallout 변화를 시각화한 자료 // 그래프가 좌상점에 가까울수록 좋은 모델
  + AUC (Area Under Curve): ROC 커브의 아래 부분 면적 비율 // 1에 가까울수록 좋은 모델


### 강화학습
- 대상
  + 상태 (S): 현재 시점에서 상황
    * 초기상태 (initial state): 에이전트가 환경과 처음 상호작용할 때의 상태
    * 종료상태 (terminal state): 에이전트가 더 이상 행동이 불가능한 상태
    * 에피소드 (episode, rollout, trajectory): 초기상태부터 종료상태까지 거친 행동 sequence
  + 행동 (A): 취할 수 있는 석택지
  + 보상 (R): 행동에 대한 이득 // 즉각적인 보상 ONLY. 장기적인 보상이 아님.
  + 에이전트 (agent): 행동을 취하는 주체 (플레이어 , 캐릭터 등)
  + 정책 (policy): 에이전트가 행동을 선택(판단)하는 방침
  + 환경 (environment): 문제 세팅 S, A, R 포함
  
