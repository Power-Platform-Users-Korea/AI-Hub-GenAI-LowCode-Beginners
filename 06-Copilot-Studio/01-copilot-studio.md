# 04. Microsoft Copilot Studio를 사용하여 코파일럿 만들기
34분, 모듈, 2개

이 모듈에서는 Microsoft Copilot Studio를 사용하여 코파일럿을 만드는 방법을 설명합니다. Copilot Studio는 자연어를 사용하여 코파일럿을 만드는데 사용할 수 있는 새로운 기능입니다. GPT-3의 강력한 기능을 사용하여 코파일럿을 위한 주제, 트리거 문구 및 응답을 생성합니다. 또한 이 모듈에서는 Conversation Booster 기능을 사용하여 코파일럿 응답을 개선하는 방법을 간략하게 설명합니다.

- 소개 : 2분
- 연습 - 새로운 AI 기능을 사용하여 Microsoft Copilot Studio에서 봇 구축 : 25분

## 1. 소개
2분

코파일럿을 구축할 때 주제, 트리거 문구 및 응답을 생성해야 합니다. 이 프로세스는 시간이 많이 걸릴 수 있습니다. 이제 Microsoft Copilot Studio에서 주제를 만드는 것이 이전보다 훨씬 쉬워졌습니다. 자연어를 사용하여 주제에서 수행하려는 작업을 설명함으로써 Microsoft Copilot Studio에서 주제를 만들 수 있습니다. 그런 다음 Microsoft Copilot Studio의 Copilot 기능에 대해 만들기를 선택하여 해당 항목을 자동으로 빌드함으로써 항목을 만드는 수동 단계를 줄일 수 있습니다.

> 대화 부스터 소개    
> 대화 부스터(Conversation Booster)는 코파일럿의 반응을 향상시킬 수 있는 새로운 기능입니다. 이를 통해 코파일럿은 주제를 생성할 필요 없이 여러 소스(내부 또는 외부일 수 있음)에서 정보를 찾고 표시할 수 있습니다. 생성된 답변을 코파일럿의 기본 정보 소스로 사용하거나 작성된 주제가 사용자의 쿼리를 처리할 수 없는 경우 대체 수단으로 사용할 수 있습니다. 결과적으로 고객의 질문을 해결하지 못할 수 있는 여러 주제를 수동으로 생성할 필요 없이 기능 코파일럿을 신속하게 생성 및 배포할 수 있습니다.

​> 자세한 내용은 Conversation Booster 및 Generative를 참조하세요 .

### 2. 연습 - 새로운 AI 기능을 사용하여 Microsoft Copilot Studio에서 봇 구축
25분

이 연습에서는 Microsoft Copilot Studio에서 Copilot을 사용하여 코파일럿을 만듭니다. 또한 대화 부스터 기능을 사용하여 코파일럿의 응답을 개선하는 방법을 배우게 됩니다.

1. Microsoft Copilot Studio 에 로그인합니다 .

현재 환경이 올바른지, 미국 지역에서 제작되었는지 확인하세요.

2. 왼쪽 탐색 메뉴에서 홈을 선택한 다음 + 코파일럿 생성을 선택합니다 .

코파일럿 생성 마법사가 열립니다. 이 마법사는 이름을 지정하고, 언어를 선택하고, 선택적으로 생성적인 답변으로 대화를 강화할지 여부를 선택하여 코파일럿을 설정하는데 도움을 줍니다.

3. 코파일럿의 이름을 Real Estate Booking Service 로 지정한 다음 English를 선택하세요 .

생성적 답변으로 대화 강화 옵션 도 표시되어야 합니다.


Generative AI 창을 설정하여 코파일럿에게 지식을 제공합니다.

이 페이지에서는 즐겨찾는 부동산 웹사이트를 작성할 수 있습니다. 따라서 코파일럿을 생성한 후 코파일럿이 질문에 답변할 수 없는 경우 답변을 제공한 웹 사이트를 검색합니다. 이 접근 방식은 수동으로 주제를 생성할 필요 없이 여러 질문에 답할 수 있는 코파일럿을 빠르게 생성할 수 있는 좋은 방법입니다.

​예를 들어 다음 이미지와 같이 웹사이트( https://powerplatform.microsoft.com/ )를 제공합니다.

사용자가 "Microsoft Copilot Studio가 무엇인가요?"라고 묻는 경우, 코파일럿은 다음 이미지와 같이 웹사이트에서 답변을 검색한 후 사용자에게 제시합니다.

부동산 서비스와 관련된 웹사이트를 제공합니다. 이 기능을 사용하지 않으려면 공백으로 남겨둘 수 있습니다. 모듈의 나머지 부분에서는 이 기능을 참조하지 않습니다.

​4. 코파일럿 이름과 언어가 설정된 상태에서 만들기를 선택합니다 .

참고    
생성을 선택한 후 새 환경 내에서 첫 번째 코파일럿을 생성하는 프로세스는 최대 15분이 걸릴 수 있습니다. 후속 코파일럿은 훨씬 빠르게 생성됩니다.

​

5. 코파일럿이 생성되면 왼쪽 탐색 메뉴에서 주제를 선택한 다음 생성 드롭다운 메뉴를 선택합니다.  주제 > Copilot을 사용하여 설명에서 만들기로 이동해서 선택합니다 .

참고    
Copilot으로 만들기 옵션이 표시되지 않으면 지능형 작성 지원을 활성화해야 할 수도 있습니다.

상단 메뉴에서 설정​​ 아이콘을 선택한 후 일반 설정을 선택합니다.

Copilot 토글을 사용한 지능형 작성 지원을 켜짐 으로 설정합니다.

6. 주제 이름을 지정 하고 주제 만들기... 공간 에 설명을 제공하라는 새 창이 나타납니다.

7. 주제 이름 지정 필드 에 다음 텍스트를 입력합니다.

Book a Real Estate Showing

부동산 쇼룸 예약하기

8. 주제 만들기... 필드에 다음 텍스트를 입력합니다.

collect a user's full name, email, address of the property, and date and time of the showing

사용자의 성명, 이메일, 숙소 주소, 예약 날짜 및 시간을 수집합니다.
​
만들기 를 선택합니다 .

생성된 트리거 문구와 함께 새 주제가 표시됩니다.

참고   
생성된 콘텐츠는 이 실습에 표시된 것과 다르게 나타날 수 있다는 점을 기억합니다.

​여러 질문 노드, 엔터티 선택 및 변수 이름 지정도 표시되어야 합니다.

9. 이메일 주소가 무엇입니까? 질문 노드 를 찾아 선택합니다.

10. 제작 캔버스 상단에 있는 Copilot으로 편집 아이콘을 선택합니다 .

11. Copilot으로 편집 패널 의 무엇을 하시겠습니까? 필드에 다음 텍스트를 입력합니다.

​update the message to say thank you to the Name variable from the previous node and then proceed to ask the question

​이전 노드의 Name 변수에 감사하다는 메시지를 업데이트한 다음 질문을 계속 진행합니다.

업데이트를 선택합니다.

메시지는 이전 메시지 노드의 이름 변수를 포함하도록 업데이트되어야 합니다.

새 노드를 추가하는 것 외에도 Copilot을 사용하여 기존 노드를 업데이트할 수 있습니다.

​12. 노드 주위의 빈 공간을 클릭하여 노드가 선택되지 않았는지 확인하십시오. Copilot으로 편집 패널 의 무엇을 하시겠습니까? 필드에 다음 텍스트를 입력합니다.
​
summarize the information collected in an adaptive card

​적응형 카드에 수집된 정보를 요약합니다.

업데이트를 선택합니다 .

적응형 카드가 있는 메시지 노드가 항목 끝에 추가됩니다.

13. 적응형 카드를 선택합니다. 적응형 카드 속성이 화면 오른쪽에 나타나야 합니다.

적응형 카드 수식은 위와 유사해야 합니다. 그렇지 않은 경우 아래 수식을 복사하여 붙여 넣을 수 있습니다.

{
type: "AdaptiveCard", 
   body: 
   [
       {
           type: "TextBlock",
           size: "Medium",
           weight: "Bolder",
           text: "Summary"    
       },
       {
           type: "FactSet",
           facts: 
           [
               {
                   title: "Full Name",
                   value: Text(Topic.FullName)
               },
               {
                   title: "Email Address",
                   value: Text(Topic.Email)
               },
               {
                   title: "Property Address",
                   value: Text(Topic.PropertyAddress)
               },
               {
                   title: "Showing Date and Time",
                   value: Text(Topic.ShowingDateTime)
               }
           ]
       },

       {
           type: "TextBlock",
           text: "Thank you for providing the information."
       }
   ]
}

14. 적응형 카드 속성을 열면 Copilot으로 편집 패널이 닫힙니다. 따라서 다시 열려면 아이콘을 선택해야 합니다. 무엇 을 하시겠습니까? 필드에 다음 텍스트를 입력합니다.
​
add a multiple choice question to confirm if the user's information is correct with the option to select either "Yes" or "No"

객관식 질문을 추가하여 "예" 또는 "아니오"를 선택할 수 있는 옵션으로 사용자 정보가 정확한지 확인합니다.​

업데이트를 선택합니다 .

사용자가 선택할 수 있는 옵션이 포함된 새 질문 노드가 항목 끝에 추가됩니다.

15. 작성 캔버스의 왼쪽 상단에서 주제 이름을 Book Real Estate Showing Topic 으로 바꿉니다 .

16. 저장을 선택하여 변경 사항을 저장합니다.

​
17. 화면 왼쪽 하단에 있는 코파일럿 테스트 버튼을 선택하여 테스트 패널을 엽니다.

​
18. 대화 시작 메시지가 나타나면 코파일럿이 대화를 시작합니다. 이에 대한 응답으로 생성한 주제에 대한 트리거 문구를 입력하세요.

I want to book a real estate showing

​부동산 쇼를 예약하고 싶습니다.

코파일럿은 "당신의 이름은 무엇입니까?"라고 대답합니다. 질문은 다음 이미지와 같습니다.

19. 나머지 정보를 입력하세요.

Full name: <Your name>   
Email address: <Your email address>    
Address: 555 Oak Lane, Denver, CO 80203   
Date and Time: 10/10/2023 10:00 AM   

20. 정보를 입력하면 다음 이미지와 같이 적응형 카드에 입력한 정보, 정보가 올바른지 묻는 질문, 예 또는 아니요 선택 옵션이 표시됩니다.

옵션을 선택한 후 Microsoft Power Automate 흐름을 통해 또는 사용자가 입력한 정보가 포함된 이메일을 사용자에게 보내 Dataverse에 데이터를 저장하는 주제를 추가로 개발할 수 있습니다. 그러나 이러한 작업은 이 모듈의 범위를 벗어납니다.
