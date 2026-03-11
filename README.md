political_news_filter  
Apply NLP to filter political news

# Introduction
최근 온라인 뉴스 플랫폼의 확산으로 인해 뉴스 데이터의 양이 급격히 증가하고 있다.  
특히, 온라인으로 만나는 정치 뉴스는 그 자극성 때문에 사람에 따라 불쾌감을 주는 경우가 존재한다.  
본 프로젝트에서는 자연어 처리(NLP)를 활용하여 정치 뉴스 자동 필터링 모델을 구축하고자 한다.

# Related Work
### 키워드 기반 필터링  
  | 장점 | 단점 |
  |-----|-----|
  |데이터 없이도 가능|정확도 낮음|
  | |문맥 이해 못함|  
  
  가장 기초적인 방법이나, 정치와 관련된 말만 들어가면 정치 뉴스로 볼 가능성이 있다.

### 전통적인 머신러닝 방법
  - Naive Bayes
  - SVM
  - Logistic Regression
    
    | 장점 | 단점 |
    |-----|-----|
    |구현 간단|문맥 이해 부족|
    |속도 빠름| |

### 딥러닝 기반 방법
  - LSTM
  - CNN
```
뉴스 (Input)
    ↓
Embedding
    ↓
  LSTM
    ↓
Classifier
    ↓
정치 / 비정치 (Output)
```

  |장점|단점|
  |---|---|
  |문맥 이해 가능|전체 학습 데이터 필요|

### Transformer 기반 모델 ⭐
#### 현재 NLP에서 가장 성능이 좋음
- BERT
- KoBERT
- KLUE-BERT
```
뉴스 텍스트
    ↓
Tokenizer
    ↓
BERT / KoBERT
    ↓
CLS embedding
    ↓
Classifier
    ↓
정치 / 비정치
```
| 장점 | 단점 |
|------|------|
| 문맥 이해 매우 좋음 | 연산량 많음 |
| 최신 NLP 방식 | |
  
딥러닝 기반 방법과 큰 차이는 사용할 때 Fine-tuning용 데이터만 가지고 있으면 된다.  
즉, 적은 데이터로 학습가능 하기에 이 프로젝트의 모델로 결정  
특히 KoBERT는 한국어 데이터로 사전학습된 BERT 모델로,  
한국어 자연어 처리 작업에서 높은 성능을 보이는 것으로 알려져 있다.
따라서 본 프로젝트에서는 적은 학습 데이터로도  
높은 성능을 기대할 수 있는 Transformer 기반 모델을 사용하며,  
특히 한국어 특화 모델인 KoBERT를 기반으로 정치 뉴스 필터링 모델을 구축한다.

# Method
본 연구에서는 KoBERT 기반 텍스트 분류 모델을 사용하여  
뉴스를 정치 / 비정치로 분류한다.  
  
뉴스 텍스트는 KoBERT tokenizer를 통해 토큰화되며,  
KoBERT 모델의 CLS 토큰 임베딩을 사용하여  
최종 분류를 수행한다.
```
뉴스 텍스트
    ↓
Tokenizer
    ↓
KoBERT
    ↓
CLS embedding
    ↓
Linear Layer
    ↓
정치 / 비정치
```

# Dataset

# Experiment

# Result

# Counclusion
