# 00. 파워 오토메이트 플로우 코파일럿을 사용하여 프롬프트로 흐름 만들기

이 모듈은 본격적인 내용에 들어가기 전 준비 운동으로 진행됩니다. 파워 오토메이트 플로우 코파일럿을 사용하여 프롬프트로 간단한 흐름을 만드는 과정을 살펴보겠습니다.

- 소개 : 2분
- 연습 – 코파일럿으로 플로우 만들기 : 30분

## 1. 소개
2분

파워 오토메이트의 코파일럿 기능을 사용하면 자연어 프롬프트를 통해 플로우를 만들 수 있습니다. 이 AI 기반 도구를 사용하면 각 단계를 수동으로 구성할 필요 없이 빠르게 자동화를 설정할 수 있습니다. 이 연습에서는 코파일럿을 사용하여 Excel 파일에서 이메일 주소를 가져와 이메일을 보내는 간단한 플로우를 만들어 보겠습니다.

## 2. 연습 – 코파일럿으로 플로우 만들기
30분

이 연습에서는 파워 오토메이트의 코파일럿 기능을 사용하여 플로우를 만들게 됩니다. Excel 파일을 OneDrive에 업로드한 다음, 코파일럿을 사용하여 이 파일에서 데이터를 읽고 이메일을 보내는 플로우를 만들 것입니다.

1. 좌측 와플 메뉴 클릭
   - Microsoft 365 앱 실행기가 열립니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/87b77d03-d0f5-4d57-b3a0-3562e587cd66)


2. OneDrive 선택
   - OneDrive가 새 탭 또는 창에서 열립니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/a2a0c319-07ef-4adc-b5e7-a32557423a02)


3. Add new 선택
   - 일반적으로 OneDrive 인터페이스 상단 근처에 있습니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/b7b027c3-fb55-4b53-85e0-e121ed1537f0)


4. 파일 업로드
   - 이 연습에 사용할 Excel 파일을 업로드합니다.해당 파일은 [여기서](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/blob/a9ecda93146c9901d525e2999f9698b9eeb76401/05-Power-Automate-Copilot/mail_list.xlsx) 다운로드 하시면 됩니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/c296844a-355e-4612-a6e1-a57dd1b7b955)
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/fc680690-949d-4192-81cc-f2dea82c3f02)


5. 좌측 와플 메뉴 클릭
   - Microsoft 365 앱 실행기로 돌아갑니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/549cb32b-e152-498c-a1a4-23945b2ee434)


6. 파워 오토메이트 실행
   - 파워 오토메이트가 새 탭 또는 창에서 열립니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/4b607755-85f8-4e54-ab1f-474cd70f6266)


7. 개발자 환경(AIHUB-US) 선택
   - 이 연습에 맞는 올바른 환경에서 작업하고 있는지 확인합니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/2f22e91d-7811-4041-81ed-b714cc3ebf95)

8. 코파일럿 채팅에 다음 프롬프트를 입력합니다:

```
엑셀에서 메일주소를 가저와 메일로 발송
```
   - 코파일럿이 이 프롬프트를 바탕으로 플로우를 만들기 시작합니다.
     ![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/a933cc32-d7aa-46e4-9a88-87f8c8f5dad7)


9. 플로우가 만들어지면 넥스트 클릭
   - 플로우 생성 과정의 다음 단계로 넘어갑니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/b7249b7e-940a-4f38-af0b-af10eadee7fb)
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/6a674761-6902-4c26-83a7-bf6495b13415)


10. Create Flow 선택
    - 초기 플로우 생성을 완료합니다.

11. List rows present in a table 선택
    - 이 작업은 Excel 파일에서 데이터를 읽습니다.

12. Location* 클릭
    - 파일 위치 선택 드롭 다운 메뉴가 열립니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/cddf1fc3-9a7f-4d88-9e74-6e816cc9da8d)


13. OneDrive for Business 클릭
    - OneDrive for Business를 지정합니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/9b3fe7d5-cb23-4f9b-b679-56f74ea327d9)


14. Document Library에서 OneDrive 클릭
    - Document Library에서 OneDrive 선택합니다.

16. Open folder 클릭후 파일 선택
    - 앞서 업로드한 Excel 파일을 선택합니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/05ca7016-4a35-4824-9049-aea22121302c)


18. 테이블 클릭
    - Excel 파일 내에서 이메일 주소가 포함된 특정 테이블을 선택합니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/7bca1128-ca66-478d-ba5c-6f66458eb874)


19. Select Query 값이 있으면 삭제
    - Query 값 삭제
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/cbd74f47-dc95-43a5-9e8e-1720af889ff0)


20. Send an email 클릭후 To의 빈값 클릭하고 번개표시 클릭
    - 동적 콘텐츠 메뉴가 열립니다.
     ![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/4485ef1b-c052-450c-b27a-ce02960a2fbf)
 

22. 메일주소 클릭
    - Excel 파일의 이메일 주소를 사용합니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/41561197-aefd-409c-af75-df673253a29e)


23. Subject에 빈값 클릭하고 번개 표시 클릭
    - 이메일 제목에 동적 콘텐츠를 추가할 수 있습니다.

24. 이름 클릭
    - 수신자의 이름으로 이메일 제목을 개인화합니다.

25. 나머지 제목 작성
    - 제목에 추가하고 싶은 텍스트를 입력합니다.

26. 수동실행을 주기적 실행으로 변경해보겠음
    "Manually trigger a flow" 선택
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/d70d1e50-c2d5-441a-9535-638afe43dea6)


27. 코파일럿 채팅에 다음 프롬프트를 입력합니다:

```
하루에 한번 주기적으로 실행되게 해줘
```
   - 코파일럿이 플로우를 일일 일정으로 실행되도록 수정합니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/30c5adfd-9e9f-4137-b9e6-9e8a1b33aff4)


28. Recurrence 선택하여 시간설정
    - 플로우가 매일 실행될 시간을 구성합니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/e48b7e0d-22f7-47b6-b766-c2ce4067f3d0)


29. 저장
    - 변경한 내용을 모두 저장합니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/a8457b35-2829-464c-bf66-ec5e14c90a25)


30. 테스트 선택하고 Manually 선택
    - 수동 테스트 실행을 준비합니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/d9503b84-8e78-4fdb-a054-b90500c364df)


31. Test 클릭
    - 테스트를 시작합니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/d2a55237-23c7-4f6b-85e0-89aa5f7880c9)


32. Run Flow 선택
    - 플로우를 실행합니다.

33. 테스트 결과 확인
    - 출력을 검토하여 플로우가 예상대로 작동하는지 확인합니다.
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/ab8eb896-9496-40c4-8f22-27c70161f851)
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/4619a14e-e821-4810-b54f-4872f36f8859)
![image](https://github.com/Power-Platform-Users-Korea/AI-Hub-GenAI-LowCode-Beginners/assets/123848060/067e041f-3a62-4f52-b488-1e00b2d3cea1)


이 단계들을 따라하면 코파일럿을 사용하여 Excel 파일에서 이메일 주소를 읽고 매일 이메일을 보내는 플로우를 만들 수 있습니다. 이 연습은 파워 오토메이트에서 AI 지원을 사용하여 유용한 자동화를 만드는 힘과 단순함을 보여줍니다.
