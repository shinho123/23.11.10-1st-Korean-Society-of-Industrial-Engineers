# 23.11.10-1st-Korean-Society-of-Industrial-Engineers
대한산업공학회(UNIST) - 다중 역할 경험을 고려한 게임 유저 이탈 예측: 롤 게임을 중심으로, 1저자

## *목차*
  1. 서론 - 연구배경, 연구동기, 연구목적
  2. 프레임워크
  3. 연구 방법
  4. 연구 결과
  5. 결론

## *연구배경*

  ### 게임 산업 시장 동향
  + 게임 산업은 지난 20년 동안 PC, 모바일, 온라인 등 다양한 플랫폼을 통해 글로벌 엔터테인먼트 경제에서 주요한 역할을 하고 있음
  + 또한, 코로나바이러스(COVID-19) 전염병에 의해 비대면 활동 및 재택 근무가 증가하면서 자연스럽게 온라인 게임 및 관련 활동의 소비가 75% 증가하였음
  + 한국콘텐츠진흥원의 글로벌 게임 산업 트렌드 보고서에 따르면(한국콘텐츠진흥원, 2023) 2020년~2022년 게임시장 수익은 이전 대비 규모가 430억 달러이상 상회하고 있으며, 팬데믹으로 인해 다양한 장르의 게임이 주목받기 시작함

  ### 게임에서 유저 이탈의 정의 및 중요성
  + 이탈 분석은 소매업, 은행업, 인터넷 서비스, 서비스, P2P, 네트워크, 보험 및 기타, 통신 부분에서 많이 활용되며, 특히 게임 부분의 이탈예측이 중요하게 나타남
  + 게임에서의 유저 이탈은 사용자의 비활성 기간을 의미하며, 게임에서는 유저가 장기간 접속하지 않은 상태를 의미함
  + 게임에서 이탈의 주된 요인은 게임 플레이 불만족, 피로감, 밸런스, 커뮤케이션 문제 등이 있음
  + 유저 이탈을 예측하기 위해 수명 주기 기반 방식, 플레이어 행동 패턴 분석 등이 활용되어 왔음
  
    + 고객 회전율이 높은 게임시장에서는 기존 고객 유지가 신규 유저의 유입보다 경제적인 선택임
    + 실제 고객 유지율이 1% 증가하면 수익이 크게 증가하는 것으로 나타남
    + 신규 고객을 확보하는데 드는 비용의 경우 기존 고객에게 추가로 판매하는 것보다 5배 더 높게 나타남
    + 유저의 구매활동은 기업 매출과 직접적인 연관이 있으므로 이탈 예측은 모든 기업에서 해결해야하는 과제로 인식됨    
    + 장기 유저는 서비스 비용이 덜 들고 더 많이 구매하는 경향이 있으며 다른 잠재유저에게 홍보할 가능성이 더 높음
   
## *연구동기*
+ 게임 이탈을 예측하는 연구의 경우 주로 시계열 및 유저의 활동 패턴을 파악한 연구가 주로 수행되어 왔음
  
  + 게임 이탈자의 세션 활동을 분석하여 일반 유저와 활동 특성을 비교하였음
  + 이탈 예측을 위해 게임 내에 시간 소비 규칙 패턴을 평가하였음
  + 유저의 구매활동, 소셜활동에 초점을 두어 게임 이탈 예측을 수행함
 
## *연구목적*
+ 본 연구는 lol(League of legend)의 데이터를 바탕으로 게임 내 다중 역할 경험을 고려한 이탈 예측 모형을 구축하고, 이를 바탕으로 개인화된 유저 관리 전략 및 시사점 제공을 목표로 함

## *프레임워크*

![image](https://github.com/shinho123/23.11.10-1st-Korean-Society-of-Industrial-Engineers/assets/105840783/b1e45f3b-2c25-4d22-868e-7c1b98efbff6)

## *연구결과*

### Baseline, Suggested model 비교

![image](https://github.com/shinho123/23.11.10-1st-Korean-Society-of-Industrial-Engineers/assets/105840783/5ab32f25-74cf-49b0-8fa1-c1a242631dc3)

+ 연구에서 제안한 모델의 경우 다중 역할 변수를 고려하지 않은 baseline model 보다 4개의 지표(Accuracy, Recall, Precision, F1-score) 대부분에서 좋은 성능을 보이고 있음
+ 즉, 게임 내에서 유저의 다중 역할 경험들이 실제 게임 이탈에 있어 중요 요인으로 작용하는 것을 알 수 있음

### 데이터 샘플링 비교

![image](https://github.com/shinho123/23.11.10-1st-Korean-Society-of-Industrial-Engineers/assets/105840783/6e0e6f8d-abb1-4f02-ab02-e08f8e83d720)

+ 오버샘플링(SMOTE)을 진행한 모델과 성능을 비교하였을 때, 오버샘플링을 진행한 모델의 성능이 근소우위로 더 높게 나타나고 있음
+ 하지만 두 모델간의 성능 차이가 크지 않은데, 이는 제안된 모델이 데이터의 불균형 문제를 잘처리하고 안정적인 예측 성능을 보이고 있는 것으로 사료됨
+ 따라서 추가로 샘플링 작업을 진행하지 않고 현재 제안된 모델을 그대로 사용하는 것이 적절한 

### 변수 중요도 표(DT, RF, XGB, GB)

![image](https://github.com/shinho123/23.11.10-1st-Korean-Society-of-Industrial-Engineers/assets/105840783/3046911e-7d61-405b-b24e-c9374f5b7194)

## *결론*

### 연구 목적
+ 본 연구는 lol(League of legend)의 데이터를 바탕으로 게임 내 다중 역할 경험을 고려한 이탈 예측 모형을 구축하고, 이를 바탕으로 개인화된 유저관리 전략 및 시사점 제공을 목표로 하였음

### 실험
+ 실험을 위해 유저 활동 변수 + 유저 다중 역할 변수로 데이터 셋을 활용하였고, 분류 성능 측정 결과 유저 활동 변수로만 구축했을때 보다 우수한 성능을 보였음
+ 또한 제안한 모델의 경우 안정적인 예측 성능을 보여 추가적인 데이터 샘플링이 필요하지 않음

### 변수 중요도
+ **유저 활동 변수 관점** : ‘summonerLevel(유저 레벨)’, ‘League_points(리그포인트)’, ‘magic_box_contents(마법 공학상자 획득 가능 개수’
+ **다중 역할 변수 관점** : ‘champion_roll_num(유저 챔피언 포지션 숫자)’, ‘user_cp_portion_marksman(원거리 딜러 활용 비율)’, ‘user_cp_portion_tank(탱커 활용 비율)'

### 연구 시사점
+ 게임 내에서 유저가 플레이 할 수 있는 역할의 수에따라 실제 게임 이탈에 영향을 주는 요인으로 확인 되었음
  + 한가지 역할만 플레이하는 유저 : 기업에서 한가지 역할만 플레이하는 플레이어들에 대한 맞춤형 게임 가이드 및 활용 자료를 제공하는 것이 요구됨
  + 다수의 역할을 플레이하는 유저 : 다양한 역할의 플레이를 요구하거나 변칙적인 플레이가 필요한 게임 컨텐츠를 신규로 생성하는 것이 요구되며, 이는 다수의 역할을 플레이하는 유저에게 게임 참여도 및 흥미를 높일 수 있음
+ 또한, 게임 플레이 시 특정 역할(탱커, 원거리 딜러)을 수행하는 챔피언들의 활용 비율에 따라 유저 이탈 관련한 유의미한 요인으로 작용하였음
  + 리그오브레전드에서 무료로 플레이 가능한 로테이션 챔프에 원거리 딜러 및 탱커 챔피언들을 포함하여 현재보다 활용 비율을 늘리고 해당 역할을 수행하는 신규 챔피언을 지속적으로 업데이트 해야함
  + 한개의 역할을 지속적으로 플레이하는 것은 피로감을 불러올 수 있으나, 다양한 신규 챔피언들의 출시로 인해 지속적인 흥미를 유발시키며, 오히려 한 가지 역할에 대한 유저의 전문성을 높일 수 있음

### 연구의 한계점 및 추후 방향
  #### 연구의 한계점
  + 현재 연구에서 사용된 다중 역할 변수로 현재 모델에서 도출된 이탈 예측의 원인을 모두 설명할 수 없으며 이는 이탈 원인이 게임이 아닌 개인·사적인 문제인 경우도 많이 존재하기 때문임
    + 이탈 예측 원인 파악을 위한 폭넓은 해석이 가능하도록 새로운 다중 역할 변수를 지속적으로 생성 및 개선해야함
  + 회사마다 보유한 게임 데이터의 종류가 다르기 때문에 연구에서 구축한 모델의 경우 다른 분야의 게임 모델에 적용하기에 한계가 있음
    + 해당 게임 기업에서 수집 가능한 데이터를 재수집하고 데이터에 맞도록 새로운 변수를 다시 생성해야함
  
  #### 추후 방향
  + 다중 역할 변수 뿐 아니라 새로운 유저들의 활동 변수도 같이 보완하여, 현재보다 더 성능을 높이고 다양한 관점에 이탈 예측 분석 수행을 목표로 하고있음
  + 추가적인 데이터 확보를 통해 모델의 안정성을 높여야 함
  + 유저들의 심리상태를 반영할 수 있는 새로운 변수 생성을 목표로 하고있음
    + 유저의 게임 소셜 활동기록(커뮤니티 댓글)을 수집 → 감정 분석 수행 후 positive 및 negative 수치 반영


