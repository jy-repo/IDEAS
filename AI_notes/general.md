# 성능 지표
  + 정밀도 (precision): True 라고 예측한 값 중 실제 True 인 값의 비율. // 찾을 것들 중 진짜 비율
  
      precision = TP / (TP + FP)
  
  + 재현율 (recall): 전체 True 중에 모델이 True 라고 예측한 값 비율.  // 찾아야 할 것들 중 찾은거 비율 
 
      recall = TP / (TP + FN)
      
  + 정확도 (accuracy): 전체 예측 값과 정답 중 옳게 예측한 값 비율.  // 찾아야 할 것과 찾은 것 중 맞춘 것 비율
  
      accuracy = (TP + TN) / (TP + TN + FP + FN)
      
      ※ Object Detection 에선 TN 값 = 0.
  
  + F1 score: precision과 recall의 조화 평균.
  
      F1-score = 2 x (precision x recall) / (precision + recall)
      
  + Fall-out = FPR (False Positive Rate): 실제 False 중 모델이 True 라고 예측한 값 비율.
  
      Fall-out(FPR) = FP / (TN + FP)
      
  + ROC (Receiver Operating Characteristic) curve: Recall-Fallout 변화를 시각화한 자료 // 그래프가 좌상점에 가까울수록 좋은 모델
  + AUC (Area Under Curve): ROC 커브의 아래 부분 면적 비율 // 1에 가까울수록 좋은 모델
