# 03. Power Automate에서 Copilot을 사용하여 부동산 솔루션에 대한 흐름 구축
26분, 모듈, 3개

이 모듈에서는 Power Automate에서 Copilot을 사용하여 흐름을 생성하는 방법을 다룹니다. Copilot을 사용하여 흐름을 개선하는 방법과 예시 AI 기능을 통해 형식을 사용하는 방법을 알아보세요. Power Automate의 Copilot은 지루한 작업을 자동화하고 시간을 절약하는데 도움이 됩니다. 사용자 친화적이며 워크플로우를 더 빠르고 효율적으로 생성하는데 도움이 됩니다.

- 소개 : 2분
- 연습 - Power Automate에서 Copilot을 사용하여 승인 흐름 만들기 : 16분
- Power Automate에서 Copilot을 사용하는 경우 : 1분

## 1. 소개
2분   
Power Automate의 Copilot은 자신만의 가상 비서를 갖는 것과 같습니다. 이는 워크플로 자동화를 더욱 단순하게 만드는 강력한 기능입니다. AI와 기계 학습을 사용하여 프로세스를 분석하고 작업 및 자동화에 대한 스마트한 제안을 생성합니다. 가장 좋은 점은 Copilot의 혜택을 누리기 위해 코딩 전문가가 될 필요가 없다는 것입니다. 복잡한 프로그래밍의 번거로움 없이 효율적인 작업 흐름을 만들 수 있도록 설계되었습니다.

Microsoft Power Automate를 사용하면 생성할 흐름을 설명하고 AI 기반 대화를 통해 흐름을 개선하고 반복할 수 있습니다. Power Automate의 이 차세대 AI 기반 Copilot은 흐름 스튜디오 내부에 위치하여 구축되거나 변경되는 모든 흐름을 돕습니다.

Power Automate의 Copilot을 사용하면 흐름을 생성하는 동안 개방형 대화 환경을 사용할 수 있습니다. 구축하면서 질문을 하고 개선 및 변경에 대한 도움을 받을 수 있습니다. Power Automate의 작동 방식에 대한 특별한 지식이 필요하지 않습니다. 자연어를 사용하면 단순한 흐름부터 복잡하고 강력한 전사적 프로세스까지 모든 것을 구축하고 향상할 수 있습니다. 

## 2. 연습 - Power Automate에서 Copilot을 사용하여 승인 흐름 만들기
16분

이 연습에서는 Power Automate의 Copilot을 사용하여 부동산 표시에 대한 승인 프로세스를 자동화하는 흐름을 만듭니다. Copilot을 사용하여 새 매물이 요청될 때 부동산 중개인에게 이메일을 보내는 흐름을 만듭니다. 그런 다음 상담원은 이메일 내에서 표시 요청을 승인하거나 거부할 수 있습니다.

Copilot을 사용하여 흐름을 만들려면 다음 단계를 따르세요.

1. Power Automate 에 로그인합니다 .

![power automate](Images/power-automate-copilot-01.png)

2. Power Automate 내 홈 페이지 중앙에 있는 Copilot으로 흐름 구축 시작 의 텍스트 필드에 다음 프롬프트를 입력합니다.

```
Start and wait for approval when a Dataverse record is created.
Please also add a flow to update a Dataverse record based on conditions after approval.
```

```
request approval when a Dataverse record is created
```

생성 버튼을 선택합니다 .

![power automate](Images/power-automate-copilot-02.png)

​3. 프롬프트에서 Copilot은 검토할 수 있는 제안 흐름에 대한 개요를 제공합니다. 흐름에는 행이 추가, 수정 또는 삭제될 때 Dataverse 트리거 와 시작 및 승인 대기 단계라는 두 가지 기본 단계가 있을 것으로 예상됩니다. 흐름을 수락하려면 다음 을 선택 하고, 다른 제안 표시 를 선택할 수도 있습니다. Copilot이 아래 이미지와 유사한 흐름을 제안하는지 확인하세요.

![power automate](Images/power-automate-copilot-03.png)

4. 연결된 앱과 서비스를 검토하세요. 연결되지 않은 경우 편집하거나 수정한 다음 흐름 만들기 를 선택합니다 .

![power automate](Images/power-automate-copilot-04.png)

Copilot으로 편집 디자이너는 오른쪽에 Copilot 채팅 창과 함께 흐름과 함께 열립니다.

![power automate](Images/power-automate-copilot-04-2.png)

5. 행이 추가, 수정 또는 삭제될 때 트리거 를 선택하여, 일부 매개변수를 설정합니다 .

​화면 왼쪽 패널에는 필요한 빈 테이블 이름 매개 변수를 포함하여, 트리거 세부 정보가 표시됩니다.

![power automate](Images/power-automate-copilot-05.png)


6. 테이블 이름 드롭다운 메뉴 에서 Real Estate Shows(부동산 표시)를 검색하여 선택합니다 .
​
![power automate](Images/power-automate-copilot-06.png)

Real Estate Shows 테이블이 없는 경우, Power Apps에서 아래 설명문으로 먼저 앱을 만듭니다.

```
real estate showings을 관리하는 앱을 구축합니다. 
필수 열은 ID, address, date, time, status, agent name, client full name, and client email입니다. 열이름은 영어여야 합니다.
상태 선택 항목은 보류 중, 확정, 취소, 완료여야 합니다.
```

7. 시작 및 승인 대기 작업을 선택 합니다.

​승인 유형 매개변수가 누락되었습니다.

![power automate](Images/power-automate-copilot-07.png)

​8. 승인 유형 드롭다운 메뉴 에서 승인/거부 - 먼저 응답을 선택합니다 .

![power automate](Images/power-automate-copilot-08.png)

​승인 유형을 선택하면 이제 더 많은 매개변수를 사용할 수 있습니다.

9. Copilot 채팅 창에 다음 프롬프트를 입력합니다.

```
Add "New Request for Real Estate Showing" as the Title parameter for the Start and wait for an approval action
```

+ 시작 및 승인 대기 작업에 대한 제목 매개변수로 "부동산 표시에 대한 새 요청"을 추가합니다.​

![power automate](Images/power-automate-copilot-09.png)
​
Copilot이 메시지를 처리하는데 몇 초 정도 걸립니다. 처리가 완료되면 Title 매개변수가 프롬프트 텍스트로 채워집니다.

10. 할당 대상 매개변수에 이 실습에 사용 중인 이메일 주소를 입력합니다. 이 이메일 주소는 승인 요청을 받는 이메일 주소입니다.

![power automate](Images/power-automate-copilot-10.png)

11. 세부정보 매개변수에 다음 텍스트를 입력합니다.

```
A new request for a real estate showing has been created. Please review the details below and approve or reject the request:   
Property:    
Client:    
Client Email:    
Date: Time:   
```
```
​부동산 보기에 대한 새로운 요청이 생성되었습니다. 아래 세부정보를 검토한 후 요청을 승인하거나 거부하세요.   
주소:   
의뢰인:   
의뢰인 이메일:   
날짜:   
시간:   
```

![power automate](Images/power-automate-copilot-11.png)

12. 세부 정보 매개 변수의 Property: 옆에 커서를 놓은 다음 번개 아이콘을 선택하여 동적 콘텐츠 창을 엽니다.

![power automate](Images/power-automate-copilot-12.png)

13. 동적 콘텐츠 창 에서 자세히 보기를 선택하여 사용 가능한 동적 콘텐츠 목록을 확장할 수 있습니다.

![power automate](Images/power-automate-copilot-13.png)

14. 주소 필드를 찾을 때까지 아래로 스크롤한 다음 선택합니다. 검색 필드에 주소를 입력하여 빠르게 찾을 수도 있습니다.

![power automate](Images/power-automate-copilot-14.png)

이제 주소 동적 콘텐츠 필드가 세부 정보 매개변수 에 추가되었습니다 .   

​
15. 클라이언트 , 클라이언트 이메일 , 날짜 및 시간 필드 에 대해 동일한 단계를 완료합니다 .

나머지 필드 작업을 완료하면, 값이 다음 이미지와 유사해야 합니다.

![power automate](Images/power-automate-copilot-15.png)


16. 조건 작업을 선택합니다. 흐름에 조건 작업이 없는 경우, 승인 단계 아래에서 새 단계 삽입...(+) 버튼을 선택하여 지금 추가하세요.

![power automate](Images/power-automate-copilot-16.png)

17. 값 선택 상자를 선택한 다음 동적 콘텐츠 창 에서 결과를 선택합니다.   
​
![power automate](Images/power-automate-copilot-17.png)

18. 조건에 대해 같음을 선택한 다음, 값 에 대해 Approve(승인)을 입력합니다.

```
Approve
```

![power automate](Images/power-automate-copilot-18.png)

19. 조건의 True 및 False 분기 모두에서 Dataverse의 행 업데이트 작업이 있는지 확인하세요 .

![power automate](Images/power-automate-copilot-19.png)

Copilot이 아직 흐름에 추가하지 않은 경우 흐름에 추가해야 할 수도 있습니다.

![power automate](Images/power-automate-copilot-19-2.png)

20. 테이블 이름 드롭다운 에서 Real Estate Shows(부동산 표시)를 검색하여 선택합니다 .

![power automate](Images/power-automate-copilot-20.png)

21. 행 ID 필드를 선택한 다음 동적 콘텐츠 창 에서 부동산 표시 고유 식별자 필드를 선택합니다 .

![power automate](Images/power-automate-copilot-21.png)

Microsoft Dataverse에서 테이블을 생성할 때마다 테이블과 동일한 이름으로 열이 자동으로 생성됩니다. 이 열은 생성된 레코드(또는 행)에 대한 고유 조회 ID 역할을 합니다.
​

22. 고급 매개변수 아래에서 모두 표시를 선택합니다 .

![power automate](Images/power-automate-copilot-22.png)

23. 상태 드롭 다운 메뉴 에서 확인됨을 선택합니다 .

![power automate](Images/power-automate-copilot-23.png)

표시가 승인되면, 부동산 표시 테이블 의 상태 필드가 확인됨 으로 업데이트됩니다 .

​24. 조건의 False 분기 아래에서 Dataverse에 대한 행 업데이트 작업을 선택합니다 . (빠진 경우 이 작업을 추가하세요.)

![power automate](Images/power-automate-copilot-24.png)

​25. 테이블 이름 드롭다운 메뉴 에서 Real Estate Shows(부동산 표시)를 검색하여 선택합니다 .

![power automate](Images/power-automate-copilot-25.png)

​26. 행 ID 필드를 선택한 다음, 동적 콘텐츠 창 에서 부동산 표시 고유 식별자 필드를 선택합니다 .

![power automate](Images/power-automate-copilot-26.png)

​27. 고급 매개변수 아래에서 모두 표시를 선택합니다 .

![power automate](Images/power-automate-copilot-27.png)

28. 상태 드롭 다운 메뉴 에서 취소됨을 선택합니다 .

![power automate](Images/power-automate-copilot-28.png)

​표시가 거부되면, 부동산 표시 테이블 의 상태 필드가 취소됨 으로 업데이트됩니다 .


--------------

29. Copilot 채팅 창에서 다음 프롬프트를 입력한 후 제출하십시오.

```
Under the "Update a row" action for both branches in the condition, add a new "Send an email (V2)" action
```
```
​조건의 두 분기에 대한 "행 업데이트" 작업 아래에 새로운 "이메일 보내기(V2)" 작업을 추가합니다. 
```

![power automate](Images/power-automate-copilot-29.png)

​몇 초 후에 Copilot은 다음 이미지와 같이 자신이 수행한 작업을 설명해야 합니다.
업데이트된 흐름이 표시되어야 합니다. 

![power automate](Images/power-automate-copilot-29-2.png)

계속하려면 이전 단계에서 연결을 수정해야 할 수도 있습니다. 계속하기 전에 오류를 수정하세요.

30. 조건의 True 분기 에서 이메일 보내기 작업을 선택합니다 .

![power automate](Images/power-automate-copilot-30.png)

​31. 받는 사람(To) 필드를 선택하고, example@example.com 이메일 주소를 제거한 다음, 동적 콘텐츠 창 에서 클라이언트 이메일 필드를 선택합니다 .

![power automate](Images/power-automate-copilot-31.png)

32. 제목 필드 의 경우, Copilot 채팅 창에 다음 텍스트를 입력한 후 키보드의 Enter 키를 누릅니다.

```
Add "Your request for a real estate showing has been approved" as the Subject parameter for the Send an email action
```
​
+ 이메일 보내기 작업의 제목 매개변수로 "부동산 표시 요청이 승인되었습니다"를 추가합니다.

![power automate](Images/power-automate-copilot-32.png)

제목 필드 는 프롬프트 텍스트로 채워져야 합니다.

![power automate](Images/power-automate-copilot-32-2.png)

33. 본문 필드 의 경우 Copilot 채팅 창에 다음 텍스트를 입력한 후 키보드의 Enter 키를 누릅니다.

```
Add "Good day - Your request for a real estate showing has been approved. Please see below for details." as the Body parameter for the Send an email action
```

+ 이메일 보내기 작업의 본문 매개변수로서 "좋은 하루 되세요 - 부동산 공개 요청이 승인되었습니다. 자세한 내용은 아래를 참조하세요."를 추가하세요.

![power automate](Images/power-automate-copilot-33.png)

본문 필드 는 프롬프트 텍스트로 채워져야 합니다.

34. 본문 텍스트 뒤에 다음 내용을 입력합니다 .

```
Property:
Agent Name:
Showing Date:
Showing Time:
```

주소:   
Agent 이름:   
표시 날짜:   
표시 시간:   

동적 콘텐츠 창의 주소 , Agent 이름 , 날짜 및 시간 필드를 본문 텍스트 의 해당 줄에 추가합니다 .

![power automate](Images/power-automate-copilot-34.png)
​
35. 동적 콘텐츠 창의 응답 요약 필드를 본문 텍스트 끝에 추가합니다 .

![power automate](Images/power-automate-copilot-35.png)

36. 조건의 False 분기 에서 이메일 보내기 작업을 선택합니다 .

![power automate](Images/power-automate-copilot-36.png)

37. 받는 사람 필드를 선택하고 example@example.com 이메일 주소를 제거한 다음 동적 콘텐츠 창 에서 클라이언트 이메일 필드를 선택합니다 .

![power automate](Images/power-automate-copilot-37.png)

​38. 제목 필드 의 경우 Copilot 채팅 창에 다음 내용을 입력한 후 키보드의 Enter 키를 누릅니다.

```
Add "Your request for a real estate showing has been rejected" as the Subject parameter for the Send an email action
```

​+ 이메일 보내기 작업의 제목 매개변수로 "부동산 표시 요청이 거부되었습니다"를 추가하세요.

![power automate](Images/power-automate-copilot-38.png)

Copilot은 요청한 내용을 항상 이해하지 못하므로 기대한 내용을 항상 정확하게 얻지 못할 수도 있으므로 "실행 취소"를 선택하거나 수동으로 흐름에 추가할 수 있습니다. Copilot은 사용자를 지원하도록 설계된 공동 작업 도구이지만, Copilot은 사용자가 지시한 내용을 항상 올바르게 해석하지 못할 수도 있습니다.

39. 본문 필드 의 경우 Copilot 채팅 창에 다음 텍스트를 입력한 후 키보드의 Enter 키를 누릅니다.

```
Add "Good day - Your request for a real estate showing has been rejected. Please see below for details." as the Body parameter for the Send an email action
```

+ ​이메일 보내기 작업의 본문 매개변수로 "안녕하세요 - 부동산 공개 요청이 거부되었습니다. 자세한 내용은 아래를 참조하세요."를 추가하세요.

![power automate](Images/power-automate-copilot-39.png)

어떤 이유로 Copilot이 이를 놓친 경우 실행 취소하고 다시 시도하거나 수동으로 조정할 수 있습니다.

40. 본문 텍스트 뒤에 다음 내용을 입력합니다 .

```
Property:
Agent Name:
Showing Date:
Showing Time:
```

주소:   
Agent 이름:   
표시 날짜:   
표시 시간:   

동적 콘텐츠 창의 주소 , Agent 이름 , 날짜 및 시간 필드를 본문 텍스트 의 해당 줄에 추가합니다 .

![power automate](Images/power-automate-copilot-40.png)

​41. 동적 콘텐츠 창의 응답 요약 필드를 본문 텍스트 끝에 추가합니다 .

![power automate](Images/power-automate-copilot-41.png)

42. 화면 왼쪽 상단에서 Dataverse 레코드가 생성될 때 요청 승인 텍스트를 선택하여 흐름 이름을 부동산 표시에 대한 승인 요청 으로 바꿉니다.

![power automate](Images/power-automate-copilot-42.png)

​43. 화면 명령 모음의 오른쪽 상단 부분에 있는 저장 버튼 을 선택하여 흐름을 저장합니다 .

![power automate](Images/power-automate-copilot-43.png)

44. 화면 오른쪽 상단에 있는 테스트 버튼 을 선택하여 흐름을 테스트합니다 . 수동을 선택한 다음 테스트를 선택합니다 .

![power automate](Images/power-automate-copilot-44.png)

-------------

45. 부동산 표시 요청을 제출하려면 Power Apps 의 부동산 표시 앱으로 이동하세요 .

![power automate](Images/power-automate-copilot-45.png)

​46. 앱을 실행한 다음 +새로 만들기를 선택하여 새 표시 요청을 만듭니다.

![power automate](Images/power-automate-copilot-46.png)
​
47. 다음 정보로 필드를 채우십시오.

​Agent 이름 - < random name >   
고객 성명 - < Your name >   
클라이언트 이메일 - < Your email >(이 실습에 사용하는 이메일)   
날짜 - < Any future date >   
시간 - < Any future time >   
상태 - 보류 중   
주소 - 210 Pine Road, Portland, OR 97204   

> 참고   
> 이 주소는 모듈 1의 Microsoft Excel 파일에 있는 주소 중 하나입니다. 이는 귀하가 업로드하여 부동산 주소 테이블 로 전환한 것과 동일한 파일입니다 .
> 일반적으로 부동산 주소 테이블 에 대한 조회 필드가 있지만 이 실습에서는 이를 단순하게 유지하기 위한 조회 필드가 없습니다.

​48. 화면 오른쪽 상단에 있는 확인 표시를 선택합니다.

​49. 앱을 닫으려면 오른쪽 상단에 있는 X를 선택하세요 .

​흐름이 실행되고 구축한 흐름에 제공한 이메일 주소로 승인 이메일을 보냅니다.

50. 이 실습에 사용 중인 이메일 계정에 로그인한 다음 이메일이 도착할 때까지 기다립니다.

![power automate](Images/power-automate-copilot-50.png)

> ​참고  
> 흐름이 즉시 실행되지 않으면 기다려야 합니다. 특히 첫 번째 시도에서 흐름이 트리거되는 데 최대 10분이 걸릴 수 있습니다.

승인은 다음 이미지와 유사해야 합니다.

51. 승인 을 선택합니다 .

​52. 설명을 추가한 다음 제출을 선택합니다 .

```
Sure thing. Can't wait to see you there.
```

![power automate](Images/power-automate-copilot-52.png)

흐름은 계속 실행됩니다. 행을 업데이트하고 요청자에게 이메일을 보냅니다. 요청자에게 전송되는 이메일은 다음 이미지와 유사합니다.

![power automate](Images/power-automate-copilot-52-2.png)

53. 흐름을 확인하고 이제 실행 기록에 흐름이 성공 으로 표시되어 있는지 확인합니다.


## 3. Power Automate에서 Copilot을 사용해야 하는 경우
1 분

Power Automate에서 Copilot을 언제 사용해야 하는지 아는 것은 이점을 극대화하는데 필수적입니다. Copilot은 다음과 같은 상황에서 유용합니다.

- 워크플로 간소화 및 최적화 - Copilot은 워크플로 자동화 프로세스를 단순화하고 최적화해야 할 때 유용한 도구입니다. 상황에 맞는 제안과 권장 사항을 제공하므로 광범위한 프로그래밍 지식 없이도 작업 흐름을 간소화하려는 사용자에게 이상적입니다.

- 워크플로 개발 가속화 - Copilot은 기존 흐름, 트리거, 작업 및 표현을 분석하는데 탁월합니다. 패턴을 식별하고 목표를 이해하여 워크플로 개발을 가속화하는데 도움이 됩니다. Copilot은 반복적이거나 시간이 많이 걸리는 작업을 자동화하는 방법을 제안함으로써 귀중한 시간과 노력을 절약해 줍니다.

- 새로운 가능성 탐색 - Copilot은 새로운 가능성을 탐색하고 워크플로의 기능을 확장하려는 사용자에게 유용합니다. 이는 귀하의 요구 사항을 예측하고 귀하가 고려하지 않았을 수 있는 조치를 제안할 수 있습니다. Copilot의 대체 접근 방식을 사용하면 혁신을 주도하고 Power Automate 워크플로에서 가능한 것의 경계를 넓힐 수 있습니다.
