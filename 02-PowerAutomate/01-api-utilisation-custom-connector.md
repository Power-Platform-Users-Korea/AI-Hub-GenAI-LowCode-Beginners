# 사용자 지정 커넥터란?
## 공개된 API와 [사용자 지정 커넥터](https://learn.microsoft.com/ko-kr/connectors/custom-connectors/)

>이번 실습에서는 서울시가 제공하는 공개 API 가운데 [서울시 부동산 실거래가 정보](https://data.seoul.go.kr/dataList/OA-21275/S/1/datasetView.do?fbclid=IwZXh0bgNhZW0CMTAAAR22PLbjMQhxt3Az_w5TYan-65n5HFpCtWxQF-tJHKskxGrlwq9WpwVwens_aem_ZmFrZWR1bW15MTZieXRlcw)를 활용해보고자 합니다.
>다만, 해당 API 가 json 타입을 제공하지만 호출문이 좀 불편하게 만들어져 있어서 중간에 별도로 Azure Function 이라는 서비스를 사용해서 앱을 만들고 호출하도록 하였습니다.
>@asomi7007 님께서 해당 부분에 대한 작업을 해주셨습니다.

### 1. API란?
API는 응용 프로그램 간에 데이터를 교환하고 상호 작용하기 위한 인터페이스입니다. API는 소프트웨어 개발자가 다른 소프트웨어와 통신하고 기능을 공유할 수 있도록 합니다. API는 일반적으로 웹 서비스, 라이브러리, 운영 체제 등 다양한 형태로 제공됩니다. API를 사용하면 개발자는 기존의 기능을 활용하거나 새로운 기능을 개발할 수 있습니다. API는 개발자들 사이에서 매우 중요한 역할을 하며, 다양한 서비스와 애플리케이션을 통합하는 데 사용됩니다.  

API는 이를 사용하는 사람에게 상세한 설명을 적은 문서를 공유하는데, 이런 문서를 'API (사용) 명세서'라고 합니다. 설명을 상세히 한 문서라는 뜻입니다.  
참고로 서울시의 아파트 부동산 실거래가 정보에 대한 명세서는 위 주소에서 내려받으실 수 있는데, [서울시 부동산 실거래가 정보 API 명세서](Assets/seoul_real_estate_api_desc.xlsx)에도 올려뒀습니다.  

다만, 우리는 실습의 편의를 위해서 Azure Function App을 사용해서 중간에 간소화한 [서울시 부동산 실거래가 정보 API (교육용) 명세서](http://www.eldensolution.kr/seoul-real-estate-api-doc.html)를 활용하겠습니다.

### 2. 사용자 지정 커넥터 만들기
다양한 방식으로 API 문서를 읽고 사용자 지정 커넥터를 만들 수 있습니다.  
다만 간편한 사용을 위해 OpenAPI(과거 Swagger) 파일을 활용해서 실습을 손쉽게 어려움 없이 만들고자 합니다.



