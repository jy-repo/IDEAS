# 강화 학습

### 용어
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
------------------
### Object Detection w/ Reinforcement Learning

- 결론
- 내용
  + **Active Object Localization with deep Reinforcement Learning**   
    1. Deep localization problem as Markov decision process (MDP)   
    1. 환경 (E): single image, bounding box
    1. 종료 상태: tight box around a target object
    1. 상태 (S): current visible region & past actions
        * (o, h)
        * o : feature vector of the observed region // 244 x 244 by CNN (Zeiler and Fergus)   
        * h : history of actions (10 past actions)   
    1. 보상 (R): recieve rewards for each dicision (action)
        * IoU measurement   
        * diff between s0 & s1 IoU   
    1. 행동 (A): 8 transformations that can be applied to the bbox + 1 to terminate the search process   
        * Horizontal moves: left, right   
        * Vertical moves: up, down   
        * Scale chamges: bigger, smaller   
        * Aspect ratio changes: fatter, taller
        * terminate: trigger 
      
- 참고한 자료
  + (2016) [*Reinforcement Learning for Visual Object Detection*](https://sci-hub.tw/https://ieeexplore.ieee.org/document/7780685) Stefan Mathe, Aleksis Pirinen, Cristian Sminchiseseu.
  + (2019) [*Efficient Object Detection in Large Images using Deep Reinforcement Learning*](https://www.groundai.com/project/efficient-object-detection-in-large-images-using-deep-reinforcement-learning/1) Burak Uzkent, Christopher Yeh, Stefano Ermon.
  + (2015) [*Active Object Localization with Depp Reinforcement Learning*](https://arxiv.org/abs/1511.06015) Juan C. Caicedo, Svetlana Lazebnik.

