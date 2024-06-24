# 05. AI Builder 및 GPT로 인텔리전스 추가
20분, 모듈, 3개

이 모듈에서는 AI Builder에서 GPT 기능을 사용하여 텍스트 만들기를 소개하고, Power Automate에서 지침을 작성하고 모델을 사용하는 방법을 간략하게 설명합니다.

- 소개 : 1분
- AI Builder에서 GPT 모델을 사용하여 텍스트 만들기 소개 : 2분
- 연습 - AI Builder 및 Power Automate에서 GPT를 사용하여 텍스트 생성 : 10분

## 1. 소개
1 분

AI Builder는 프로세스를 자동화하고 결과를 예측하여 비즈니스 성과를 향상시키는데 도움이 되는 Microsoft Power Platform 기능입니다. AI Builder를 사용하면 비즈니스 데이터에 연결되는 앱과 흐름에 AI를 신속하게 가져올 수 있습니다. 이는 기본 데이터 플랫폼(Microsoft Dataverse)이나 SharePoint, OneDrive 또는 Azure와 같은 다양한 Microsoft 클라우드 데이터 소스에 저장된 데이터로 작동합니다.

AI Builder에서 생성하는 AI 모델은 비즈니스를 개선하기 위한 인텔리전스를 제공하는데 도움이 될 수 있습니다. AI Builder는 기술 수준에 상관없이 누구나 코드를 작성하지 않고도 앱과 흐름에 AI 기능을 추가할 수 있기 때문에 AI 생성 환경을 단순화합니다. 또한 AI Builder는 모델을 구축하고 훈련하기 위해 데이터를 수집할 필요가 없는 사전 구축된 AI 모델을 제공합니다. 즉시 인텔리전스를 사용할 수 있습니다.

## 2. AI Builder에서 GPT 모델을 사용하여 텍스트 생성 소개
2분

AI Builder에서 GPT를 사용하여 텍스트 생성 모델 은 GPT(Generative Pre-trained Transformer) 기술을 기반으로 구축된 Microsoft Azure OpenAI 서비스를 기반으로 하는 텍스트 생성 모델입니다. GPT 모델은 자연어 처리 모델의 한 유형입니다.

GPT 모델은 프롬프트에서 인간과 유사한 텍스트를 생성하기 위해 대규모 콘텐츠 본문을 훈련하였습니다. 이를 워크플로 자동화와 결합하면 GPT와 같은 AI 모델을 사용하여 다양한 작업을 자동화할 수 있습니다.

예를 들어 이메일 초안, 고객 서비스 응답 및 제품 설명을 자동으로 생성하는 워크플로를 구축할 수 있습니다. 또한 워크플로를 사용하여 고객 서비스 상담원이 고객 문의에 신속하게 응답할 수 있는 스크립트를 생성할 수도 있습니다.

AI Builder에서 GPT를 사용하여 텍스트 생성 모델에 대한 프롬프트를 생성할 때 프롬프트는 두 부분으로 구성된다는 점을 기억해야 합니다.

+ 지침 - 모델이 수행해야 할 작업을 알려줍니다.
+ 문맥(컨텍스트) - 모델이 지침을 따르는데 필요한 정보입니다.

자동화 작업에서는 지침이 일정하며, 동적 콘텐츠가 컨텍스트를 제공합니다.

## 3. 연습 - AI Builder 및 Power Automate에서 GPT를 사용하여 텍스트 생성
10 분

이 연습에서는 AI Builder에서 GPT로 텍스트 만들기 모델을 사용하여 고객이 부동산 표시를 요청하며 보낸 이메일에서 정보를 추출하는 Microsoft Power Automate 흐름을 구축합니다. GPT를 사용한 텍스트 생성 모델은 고객의 이름, 고객이 보려는 부동산의 주소, 표시 날짜 및 시간을 이메일에서 추출합니다. 그런 다음 모델은 추출된 정보와 함께 Microsoft Teams 채널에 메시지를 보냅니다.

이 추출된 정보를 사용하여 Dataverse 테이블에 레코드를 생성할 수 있습니다. 그러나 해당 작업은 이 실습의 범위를 벗어납니다.

1. Power Automate 에 로그인합니다 .

2. 왼쪽 창에서 만들기 > 자동화된 클라우드 흐름을 선택합니다 .

3. 흐름 이름을 Extract Details for Real Estate Show 로 지정합니다 .

4. 모든 트리거 검색 상자 에 이메일이 도착할 때를 입력한 다음 새 이메일이 도착할 때 트리거를 선택합니다.

5. 만들기 를 선택합니다 .

​6. 새 이메일이 도착할 때 트리거 에서 고급 옵션 표시를 선택합니다 .

​7. 제목 필터 에 "[Query]"를 입력합니다.

> 참고
> 이 단계를 수행하면 이메일 제목에 "쿼리"라는 단어가 포함된 경우에만 흐름이 실행됩니다(이 랩의 목적에 따라).
> 실제 시나리오에서는 고객 문의를 처리하는 별도의 이메일 주소가 있을 수 있으므로 제목별로 필터링할 필요가 없습니다.

​8. 새 단계를 선택한 다음 AI Builder를 선택합니다 .

9. 작업 목록에서 GPT로 텍스트 생성을 선택합니다 .

10. 프롬프트 만들기를 선택한 다음 공백에서 시작을 선택합니다 .

11. 모델이 생성해야 하는 텍스트 설명 상자 에 다음 텍스트를 붙여넣습니다 .

```
Extract "Name", "Address", "Date", and "Time" from the text below.

When the text below has less than a couple of words, answer that you can't extract information.

[Start of text]
Good day,

I hope this email finds you well. My name is <Your name>, and I am currently in the market for a new property. I came across your listing for the property located at 210 Pine Road, Portland, OR 97204, and am very interested in learning more about it.

I would like to kindly request a viewing of this property on September 15th at 3:30 PM. I believe this time is within the normal hours for showings, but if there are any conflicts or alternate time suggestions, please let me know at your earliest convenience.
[End of text]
```

이전 프롬프트에서는 GPT 프롬프트( 지침 및 컨텍스트 )를 생성하기 위한 기본 공식을 사용합니다. 여기서 프롬프트의 첫 번째 부분은 지침 구성 요소입니다.

​```
Extract "Name", "Address", "Date", and "Time" from the text below. When the text below has less than a couple of words, answer that you can't extract information.
```

다음 텍스트는 수식의 컨텍스트 구성 요소입니다.

```
[Start of text] context [End of text]
```
​
명령은 모델이 수행해야 하는 작업을 알려줍니다. 컨텍스트는 모델이 지침을 따르는데 필요한 정보입니다. 자동화 작업에서 지침은 일정하며 동적 콘텐츠는 다음 단계에서 업데이트할 컨텍스트를 제공합니다.

​
12. 테스트를 선택하여 GPT가 텍스트에서 올바른 정보를 추출하는지 확인합니다.

몇 초 동안 응답을 준비한 후 GPT 모델은 다음 이미지와 같이 예제 프롬프트에서 관련 정보를 추출할 수 있어야 합니다.

13. 흐름에서 프롬프트 사용 을 선택합니다 .

​14. 프롬프트 에서 예제 이메일을 삭제 한 다음 이를 트리거 이메일의 본문 동적 콘텐츠로 바꿉니다.

이메일이 도착할 때마다 GPT는 이메일 본문에서 관련 정보를 추출하려고 시도합니다.

​AI가 생성한 콘텐츠는 사실이 부정확하거나 부적절하거나 편향될 수 있습니다. AI 생성 텍스트를 사용하는 워크플로를 어디에 게시하거나 사용하기 전에 사람의 감독을 삽입하는 관행을 도입하는 것이 좋습니다 .


이제 사람이 추출된 정보를 검토할 수 있도록 승인 단계를 추가하겠습니다.

15. 새 단계를 선택한 다음 승인을 검색하여 선택합니다 .

​16. 작업 목록에서 시작 및 텍스트 승인 대기를 선택합니다 .

​17. 제목 상자 에 추출된 정보 검토 를 입력합니다 .

18. 제안된 텍스트 상자 에서 GPT로 텍스트 만들기 작업의 텍스트 동적 콘텐츠를 추가합니다 .

19. 할당 대상 상자 에 이 실습에 사용 중인 이메일 주소를 입력합니다.

​
20. 세부 정보 상자 에 다음 텍스트를 입력합니다.

```
Please review the extracted information and edit as necessary.
```
​+ 추출된 정보를 검토하고 필요에 따라 수정하세요.

작업은 다음 스크린샷과 유사해야 합니다.

21. 새 단계 를 선택 하고 제어 를 검색한 다음 조건 을 선택합니다 .

​22. 값 선택 상자를 선택한 다음 동적 콘텐츠 창 에서 결과를 선택합니다 .

​23. 조건에 대해 같음을 선택한 다음 값 선택 에 Approve(승인)을 입력합니다 .

24. If yse(그렇다면) 상자 에서 작업 추가를 선택합니다 . Teams 를 검색 한 다음 채팅 또는 채널에 메시지 게시를 선택합니다 .

25. 게시 드롭다운 메뉴 에서 Flow bot을 선택한 다음 게시 드롭다운 메뉴 에서 Flow bot과 채팅을 선택합니다 .

26. 수신자 상자 에 이 실습에 사용 중인 이메일 주소를 입력합니다.

​
27. 메시지 상자 에 다음 텍스트를 입력합니다.

```
Please add the following Real Estate Showing Request.

Client Email:
```

+ 다음 부동산 표시 요청을 추가하세요.
+ 고객 이메일:

28. 동적 콘텐츠 추가를 선택한 다음 새 이메일이 도착할 때 작업 에서 보낸 사람 옵션을 선택합니다 .

29. 클라이언트 이메일 줄 아래의 시작에서 텍스트 시작 및 승인 대기 작업에서 허용된 텍스트 동적 콘텐츠를 선택합니다 .

이 단계에서는 클라이언트 이메일과 승인 작업의 수락됨 텍스트가 포함된 직접 Teams 메시지를 보내 Microsoft Power Apps의 부동산 표시 앱에서 레코드를 생성하도록 상기시킵니다.

추출된 엔터티를 JSON 개체로 변환한 다음 해당 개체를 사용하여 Real Estate Showings 앱 및 Dataverse 테이블에 레코드를 생성함으로써 레코드 생성을 자동화할 수 있습니다. 그러나 해당 작업은 이 실습의 범위를 벗어납니다.

​아니요 상자 에 이메일 보내기 작업 을 추가하여 상영 예약에 필요한 정보가 충분하지 않음을 발신자에게 알릴 수 있습니다. 그러나 원하는 시간에 해당 작업을 추가할 수 있습니다.

30. 지금은 흐름을 저장하고 테스트해 보세요. 저장을 선택한 다음 테스트를 선택합니다 .

31. 수동을 선택한 다음 테스트를 선택합니다 .

​32. 이메일 주소에서 제목 [Query] - New Booking Request과 다음 본문 내용을 포함하여 이 실습에 사용하는 이메일 주소로 이메일을 보냅니다.

```
Hello,

I trust you're doing well. I'm John Doe and I'm actively searching for a new home. Your listing for the property at 789 Maple Avenue, Lexington, KY 40502 has caught my attention, and I'm eager to find out more.

Could I arrange to see the property on September 29th at 1:45 PM? I think this falls within your usual showing times, but if that doesn't work for you or if you have other time options, I'd appreciate it if you could inform me as soon as possible.
Hello,

​

I trust you're doing well. I'm John Doe and I'm actively searching for a new home. Your listing for the property at 789 Maple Avenue, Lexington, KY 40502 has caught my attention, and I'm eager to find out more.

​

Could I arrange to see the property on September 29th at 1:45 PM? I think this falls within your usual showing times, but if that doesn't work for you or if you have other time options, I'd appreciate it if you could inform me as soon as possible.
```
​

33. 다음 스크린샷과 같이 자신에게 보낸 이메일과 추출된 정보가 포함된 승인 요청이 표시되는 Outlook을 엽니다.

34. 승인을 선택한 다음 Teams를 엽니다. 요청이 승인되면 다음 이미지와 같이 추출된 정보가 포함된 플로우 봇의 메시지를 받아야 합니다.

35. 흐름이 성공적인 실행을 표시해야 하는 Power Automate 흐름으로 돌아갑니다.


성공적으로 실행된 흐름을 표시하는 스크린샷입니다.
