# MJU-IAAFF

## 명지대학교 산학협력단 (Myongji University Industry And Academia Cooperation Foundation) 연구

## 연구 주제 : 과학기술, ICT 분야 동향 분석 및 주요 정책 추진에 관한 기대효과에 대한 연구 (Analysis of trends in science and technology and ICT and a study on the expected effects of major policies)

[보고서 표지] (보고서는 8월 25일 완성 예정입니다.)
![image](https://github.com/98Haeng/MJU-IAAFF/assets/81914795/ab17153b-ae54-4c45-b5c8-ac58afd79f94)

[연구 진행 기간]
- 2023.02.27 ~ 2023.08.25

[참여 역할]
- 학생 연구원(연구보조)

[연구 과정]
- 과학기술, ICT 관련 논문에 대해 1954~2023년도에 해당하는 논문을 수집하였습니다.
- 수집 후, NLTK를 이용하여 전처리를 진행한 후, 논문의 초록 데이터에서 키워드를 추출하였습니다.
  1. 소문자로 통일하는 과정, lemmatize과정을 통해 형태를 명사형으로 설정하였습니다.
  2. 저자 키워드를 기준으로, 완전일치한 단어만 추출하는 과정을 진행했습니다.
- 추출 후, 연도_키워드 형태로 변환하였습니다. (ex. 23년도의 deep_learning -> 23_deep_learning)
- 앞선 결과를 이용하여 군집을 설정하였습니다.
  1. 군집 설정을 위해서는 Word2Vec을 이용하였고, 100차원의 벡터 형태로 만들어 유사도를 구하고, 같은 년도 단어만 이용하여 군집으로 만들었습니다.
  2. 이러한 군집을 바탕으로 약 940개의 군집이 완성되었습니다.
- 해당 결과로 계통도를 구현하였고, 이를 바탕으로 군집별 변화 양상을 그래프를 통해 확인하였습니다. (엔트로피, 누적합 등)
  - 샘플 그림은 다음과 같습니다.
    ![2023Cluster_68_entropy](https://github.com/98Haeng/MJU-IAAFF/assets/81914795/a3586734-c63b-47cd-b6b8-5a7e337a4b84)


[주의 사항]
- 코드가 난잡하게 이루어져 있습니다. 전처리 및 중간중간 수정이 복잡하였기에, 양해부탁드립니다. 설명이 필요하다면 연락해주신다면 친절히 설명해드리겠습니다.
- 논문 데이터는 보안상이 아닌, 용량이 너무 커서 공유하기가 힘듧니다. (원본 데이터 기준 13.2GB...)


