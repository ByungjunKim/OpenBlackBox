# 전산사회과학 연구과정의 블랙박스 열기 Appendix

 ### 1. KCI 논문 데이터 내보내기
 KCI 논문 서지데이터를 수집하는 가장 쉬운 방법은 KCI 홈페이지에 내장된 ‘내보내기’ 기능을 활용하는 것이다. 검색어나 학문 분류 등을 통해 연구자가 원하는 조건의 논문을 검색한 후 ‘서지정보 내보내기’ 기능을 통해 txt, RefWorks, Endnote, XML 등의 형태로 서지사항을 내보낼 수 있다 (<Figure 1> 참조). 다만  KCI 논문검색이 한 페이지당 최대로 선택할 수 있는 논문 수는 300건으로 한계가 있다. 이때는 엑셀로 내보내기 기능을 이용하길 추천한다. ‘엑셀’이라고 적힌 버튼을 누르면 최대 2000건까지 한꺼번에 서지 정보를 다운 받을 수 있다. 기존 문헌정보학 연구에서는 위의 서지 정보 내보내기를 통해 데이터를 수집해 분석하였고, 수집과정에 반복 작업이 필요했다 (이재윤, 2021; 정유경, 2020; Kim, 2022). 이 당시에는 후술할 API가 제대로 구축되어 있지 않았고, 데이터 요청 과정도 구조화되어 공지되지 않았기 때문이다.

\<Figure 1\> Example of search results in KCI webpage

 KCI가 제공하는 API는 총 다섯 가지이다. 인용지수 관련 두 가지와 논문 관련 세 가지가 있는데 논문 API에는 1) 논문 기본 정보, 2) 논문 상세 정보, 3) 참고문헌 정보가 있다. 여기서는 논문 API를 중심으로 다룬다. 우선 API를 활용하려면 [API 페이지](https://www.kci.go.kr/kciportal/po/openapi/openApiList.kci)에서 <OPEN API 키신청>을 통해 API 키를 발급받아야 한다. API 이용 신청서 작성을 통해 1주일 이내 승인이 이뤄진다. 발급받은 API 키 번호를 활용해 특정 논문의 기본 정보를 가져오는 URL 예시 다음과 같다.<sup id="a1">[1](#f1)</sup>

|Sample URL: http://open.kci.go.kr/po/openapi/openApiSearch.kci?apiCode=articleSearch&key=12345678&displayCount=100&id=ART002656945 | | |
|:----|:----|:----|
|Parameter|Value|Description|
|apiCode|articleSearch|The name of API that requests basic information of articles|
|key|12345678(example)|API Key|
|displayCount|100|The number of requested papers per trial|
|id|ART002656945|Article ID|

위 예시 URL은 <Table 1>과 같이 정리할 수 있다. apiCode 파라미터는 연구자가 요청할 API의 종류를 뜻하는데 논문 기본정보의 값은 articleSearch이다. key 파라미터에는 자신의 API 키를 넣어야 한다. displayCount는 한 번에 요청할 수 있는 논문 수이며, 예를 들어 100이라고 기입하면 최대 100건의 논문이 검색된다. 위 예시에서는 id 파라미터에 특정 논문의 id를 추가했기 때문에 논문 한 건의 정보만 나온다. 위 파라미터 외에도 제목, 저자명, 저널 명 등의 다양한 파라미터를 활용해 여러 건의 논문 정보를 요청할 수 있다. API 요청 결과는 XML(Extensible Markup Language) 형태로 받아볼 수 있다. XML은 웹상에서 데이터를 쉽게 주고받을 수 있게 만든 마크업 언어이다. 태그(tag)와 요소(element)로 정보를 표현하며 파싱(parsing) 과정을 통해 연구자가 원하는 데이터를 추출 및 변형할 수 있다.<sup id="a2">[2](#f1)</sup>. 아래 예시(<Figure 3>)처럼 서지 내보내기에는 없었던 초록이나 참고문헌 정보를 API에서는 확인할 수 있다.


### 2. KRI 연구자 정보 크롤링 과정

### 3. OpenAlex 관련 구체적인 내용


### 각주
<b id="f1">1</b> API 요청 파라미터에 대한 자세한 설명은 각 API 페이지를 참고할 것. [↩](#a1)  
<b id="f2">2</b> XML에 관련한 내용은 [다음 글](https://www.webzineriks.or.kr/post/디지털-인문학-연구를-위한-공공데이터-활용-2-김병준)을 참고할 것.[↩](#a2)