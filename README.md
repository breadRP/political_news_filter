political_news_filter  
Apply NLP to filter political news

# Introduction
우리는 최근에 신문보다 온라인 뉴스를 보는 경우가 더 많아지고 있다.  
이는 옛날보다 온라인 뉴스 데이터 양이 많아지고 있기 때문이다.  
특히 온라인으로 만나는 정치 뉴스는 그 자극성 때문에 사람에 따라 불쾌감을 주는 경우가 존재한다.  
그렇기에 NLP를 이용해 이를 필터링해보는 프로젝트를 해보고자 한다.

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

### Transformer 기반 모델
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

# Method

# Dataset

# Experiment

# Result

# Counclusion
