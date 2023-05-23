# 코드 설명 및 데이터 공유 정책

### BERTopic_Comparison_Code.ipynb
[BERTopic](https://github.com/MaartenGr/BERTopic)을 활용한 KCI와 SSCI 학문장 비교 분석 코드.

### KCI_SSCI 전처리.qmd
OpenAlex와 KCI에서 수집한 SSCI와 KCI 학술지 논문 정보 전처리 코드. 2004년부터 2021년까지 발간된 논문을 분석에 활용함.

### KCI_soc.qmd
[Structural Topic Model](https://www.structuraltopicmodel.com/)을 활용한 두 학문장 비교 코드.

### 연구 데이터 공유
SSCI 데이터는 OpenAlex에서 제공하는 데이터를 활용했으나, 저작권 문제로 OpenAleX에서는 초록 데이터의 경우 온전히 제공하지 않고 [inverted index](https://en.wikipedia.org/wiki/Inverted_index)로 인덱싱을 거쳐서 공유함. 따라서 본 연구에서도 SSCI 데이터는 연구 데이터 요청(github issue 페이지 활용)시 연구 목적으로만 제공할 예정.  
KCI의 경우 API를 통해 수집한 데이터를 '220408_KCI_Sociology.csv' 파일로 업로드 함.