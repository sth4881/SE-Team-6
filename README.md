# Software-Engineering Team 6

### 👨‍💻 ‘내가 가진 식재료를 바탕으로 메뉴를 추천해주는 어플’
- 내가 보유한 식재료만으로 곧바로 조리할 수 있는 음식들을 보여줌으로써 어떤 요리를 만들 수 있을지 고민하거나 인터넷을 뒤져볼 필요가 없어진다.
- 요리를 만들고 식사를 마치면 본인이 가지고 있는 식재료에서 음식 조리에 사용된 재료는 자동으로 차감되기 때문에 식재료가 얼마나 남았는지 알 수 있고, 장을 언제 보러 가야 할지 미리 파악할 수 있다.
- 사용자는 제공되는 기존의 레시피를 이용하여 음식을 조리해먹을 수 있으며 자기만의 레시피를 만들고 다른 사용자들과 공유할 수도 있다.
또한, 다른 사용자들로부터 자기가 만든 레시피에 대한 추천과 피드백을 받을 수 있으므로 이전보다 더 나은 요리를 만들 수 있다.


### 👪 주요 고객층
- 평소에 요리에 자신이 없고 익숙하지 않은 사람들
- 한정된 식재료를 이용하여 최적의 식사를 하고싶은 자취생
- 매번 레시피에 필요한 식재료를 딱딱 맞춰서 구하기 번거로운 사람들
- 식재료가 떨어질 때쯤에는 매번 장을 언제 봐야하나 고민하고 냉장고를 들여다봐야 하는 주부들

### 🎯 기능적 요구사항
- 음식을 만들기 위해서 반드시 필요한 재료와 그렇지 않은 재료를 구분하고 만들 수 있는 요리 위주로 선별해서 보여줄 수 있어야 한다.
- 요리를 완성하면 요리에 사용된 재료를 자동으로 차감시킬 수 있어야 하고, 사용자가 보유한 재료가 얼만큼 남았는지 수치 상으로 보여줄 수 있어야 한다.
- 내가 만든 나만의 레시피를 공유할 수 있어야 하고, 다른 사용자가 공유한 레시피 또한 볼 수 있어야 한다.
- 내가 가지고 있는 식재료의 유통기한 및 보관 방법을 알려줄 수 있어야 한다.
- 내가 가지고 있는 식재료가 얼마나 남았는지 알려줄 수 있어야 한다.
- 내가 전에 조리했던 요리를 나만의 '요리 일기'에 기록함으로써 내가 며칠 전에 어떤 요리를 했는지 알 수 있어야 한다.

### 🏹 비기능적 요구사항
- 조리 가능한 요리가 다양할 경우 최근 조리 내역을 반영하여 사용자가 보다 다양한 음식을 접할 수 있어야 한다.

### 🏢 경쟁사 분석
- <https://github.com/sth4881/SE-Team-6/blob/master/%EA%B2%BD%EC%9F%81%EC%82%AC%EB%B6%84%EC%84%9D.md>

### 💻 필요한 기기
- Android OS를 지원하는 핸드폰

### 📑 Use Case Diagram
<img src="https://user-images.githubusercontent.com/69136953/93884905-74e17400-fd1e-11ea-9b24-0cfbc12aba10.png" width="1000" height="800"></img>

### 📑 Use Case Description
***Use case name*** | Receive recommendation
-- | --
***Participating actors*** | - User
***Flow of events*** | 1. User가 단말기에서 “Receive recommendation” 기능을 선택한다.<br/>                2. App은 ‘냉장고를 채워주세요.’ 라는 토스트(Toast)메시지와 함께             User의 ‘냉장고’로 화면                을 전환한다.<br/>                2.1 사전에 등록된 정보가 있는 User는 이 단계를 생략한다.<br/>   3. User는 App이 제공하는 양식에 따라 현재 보유하고 있는 재료의 종류와 수량을 카테고리에 맞게 입력한다.<br/>                4. App은 User가 입력한 정보를 토대로 Recipe Database에 접속한 후, 현재 조리 가능한                요리를 화면에 띄운다.</br>   5. User는 추천받은 요리 중 하나를 선택한다.</br>                6. App은 User에게 Recipe Database에 저장된 ‘기본 레시피’를 제공하고, 필요에 따라 다                른 User들이 공유한 레시피도 함께 제공한다. 
***Entry condition*** | - User는 App에 로그인 한다.
***Exit condition*** | - User는 App으로부터 적절한 요리(겹치는 재료가 많은)를 추천받는다. </br>   - User는 App으로부터 트랜잭션이 처리될 수 없는지에 대한 설명을 받는다.(재료부족)
***Quality requirements*** | - App은 User에게 다양한 정렬방식(댓글 순, 공유횟수)을 이용해서 메뉴를 추천할 수 있어야 한다.

### 📑 Scenario Description
<img src="https://user-images.githubusercontent.com/46771903/93951558-9e7fb700-fd81-11ea-9dfe-f1c29ad9ab00.png" width="500", height=600"></img>


***Scenario Name*** | 음식추천 받기
-- | --
***Participating actor instances*** | - Bob : 자취생
***Flow of events*** | 1. 자취를 시작한 지 얼마 되지 않은 Bob은 최근에 배달음식을 자주 시켜 먹어서 주5일 아르바이트에도 불구하고 돈이 부족한 상황에 놓이게 된다.<br/> 2. 식비를 아낄 수 있는 방법에 대해서 고민하던 Bob은 인터넷을 검색하다가 우연히 App에 대해서 알게 된다. 금일 저녁을 어떻게 해결하면 좋을지 고민하던 Bob은 App을 활용해서 요리를 해보기로 한다.<br/> 3. Bob은 며칠 전에 엄마가 가득 채워놓고 간 냉장고를 뒤지며 어떤 재료가 있는지 살피면서 ‘인벤토리’에 재료를 하나하나 등록한다.<br/>   4. 재료등록을 마친 Bob은 App이 추천해주는 여러 음식 후보 중에서 겹치는 재료가 가장 많은 김치볶음밥을 해서 먹기로 결정한다.<br/>   5. 저녁 식사를 배부르게 먹은 Bob은 참고한 레시피에 ‘추천’을 누르고 ‘덕분에 맛있게 잘 먹었습니다’라고 감사함을 표하는 댓글을 달고 App을 종료한다.

### 🤝 팀 구성
| Participants | Roles | Skills | Training Needs |
|:------------:|:-----:|:------:|:--------------:|
| 송진호 | 팀장, 서버 개발, DB 설계 및 구현 | C, Java, Python, HTML, Javascript, Node.js(Express.js), MySQL | UML 모델링 |
| 김태호 | 문서작성 및 테스터 | C, Java | UML 모델링 |
| 류준형 | 안드로이드 개발, 테스터 | C, Java, Javascript(jQuery), MySQL, PHP, Python(NumPy, Matplotlib, TensorFlow-Keras), Flask | UML 모델링 |
| 박근모 | 안드로이드 개발, 테스터| C, Java, Android, Python, HTML, CSS | UML 모델링 |

