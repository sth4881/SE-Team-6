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

### 📑 Use Case Diagram - 박근모
<img src="https://user-images.githubusercontent.com/69136953/95857079-08deb280-0d96-11eb-8bee-197408abdb18.png" width="1000" height="800"></img>

### 📑 Use Case Description - 류준형
***Use case name*** | Receive recommendation
-- | --
***Participating actors*** | User
***Flow of events*** | 1. User가 단말기에서 “Receive recommendation” 기능을 선택한다.<br/>                2.App은 Organize recipe data 유스 케이스를 호출하여 User 적          절한 요리를 선정한다.<br/>                2.1 App은 User에게 현재 조리 가능한 요리를 알려준다.<br/>   3. User는 추천받은 요리 중 하나를 선택한다.<br/>                4. App은 Send recipes 유스 케이스를 호출하여 User에게 기본           레시피와 다른 User들이                공유한 레시피를 알려준다.</br>
***Entry condition*** | - User는 App에 로그인 한다.
***Exit condition*** | - User는 App으로부터 적절한 요리(겹치는 재료가 많은)를 추천받는다. </br>   - User는 App으로부터 트랜잭션이 처리될 수 없는지에 대한 설명을 받는다.(재료부족)
***Quality requirements*** | - App은 User에게 다양한 정렬방식(추천순, 공유 횟수 등)을 이용해서 메뉴를 추천할 수 있어야 한다.

### 📑 Scenario Description - 송진호
<img src="https://user-images.githubusercontent.com/46771903/95748379-dae56980-0cd4-11eb-96ff-202b8a14c41b.png" width="700" height="740"></img>

<img src="https://user-images.githubusercontent.com/46771903/95747967-41b65300-0cd4-11eb-943f-24d461377945.png" width="700" height="770"></img>

### 📑 Sequence Diagram(ReceiveRecommendation) - 박근모
<img src="https://user-images.githubusercontent.com/69136953/95937437-c4452c80-0e12-11eb-8b79-94e8b50d2d1f.png" width="1000" height="400"></img>

### 📑 Sequence Diagram(ManagementIngredient) - 김태호
![Sequence Diagram_IngredientManagement_작성자 김태호](https://user-images.githubusercontent.com/70993226/95859609-d5058c00-0d99-11eb-919f-bf812e1018be.PNG)

### 📑 Class Diagram
**수정 전 - 류준형**
<img src="https://user-images.githubusercontent.com/62328584/95936864-80055c80-0e11-11eb-83c7-2ae468caac82.JPG" width="1000" height="500"></img>

**수정 후 - 송진호**
<img src="https://raw.githubusercontent.com/sth4881/SE-Team-6/master/img/Class%20Diagram.png" width="1000" height="450"></img>

### 📑 Object Diagram(나만의 레시피 만들고 공유하기) - 송진호
<img src="https://user-images.githubusercontent.com/46771903/95872449-c3c47b80-0da9-11eb-81ad-8aabf03c462a.png" width="800" height="550"></img>

### 📑 Design Goals - 류준형
**Performance**
- *Response Time* : 재료를 입력하는 과정에서 사용자의 수고로움이 요구된다. 그런 만큼, 입력한 재료와 수많은 레시피들을 비교하여 신속 정확하게 최적의 레시피를 제공해야 한다.
- *Throughput* : 사용자가 레시피를 업로드 실행할 때
다량의 사진 또는 동영상을 업로드하는데
막힘이 없어야 한다.

**Maintenance**
- *Extensibility* : 기존에 없던 레시피들이 미디어를 통해 화제가 되곤 한다. 새로운 레시피들을 추가하여 사용자들에게 보다 다양한 메뉴를 추천해줘야한다. 레시피 데이터베이스에 새로운 레시피를 추가하는데 용이해야한다.

**End User**
- *Usability* : 사용자가 재료를 입력하는 과정이 보다 단순하고 편리할 필요가 있다. 재료별 다양한 카테고리를 제시하고 재료 수량표시를 세분화한다.   
또한, 사용자가 레시피를 선택할때 어려움이 없어야 한다.
다양한 레시피를 목록화하여 제공하되, 카테고리별 분류를 통해
레시피 선택 시간을 줄일수게 한다. 조리에 사용된 재료는 저절로 차감되도록 한다.
또한, 사용자가 레시피를 참고하는 과정에서의 편리함도 중요하다. 요리를 진행하는 중간중간 레시피를 확인하는데 어려움이 없도록 한다.

### 📑 Component Diagram - 송진호
<img src="https://user-images.githubusercontent.com/46771903/100820814-68059d00-3492-11eb-9c65-ba9e5844c88a.png" width="1000" height="685"></img>

### 📑 Deployment Diagram - 
<img src="https://user-images.githubusercontent.com/46771903/100820831-72279b80-3492-11eb-84ad-a6f356bc01aa.png" width="1000" height="575"></img>

### 🤝 팀 구성
| Participants | Roles | Skills | Training Needs |
|:------------:|:-----:|:------:|:--------------:|
| 송진호 | 팀장, 서버 개발, DB 설계 및 구현 | C, Java, Python, HTML, Javascript, Node.js(Express.js), MySQL | UML 모델링 |
| 김태호 | 문서작성 및 테스터 | C, Java | UML 모델링 |
| 류준형 | 안드로이드 개발, 테스터 | C, Java, Javascript(jQuery), MySQL, PHP, Python(NumPy, Matplotlib, TensorFlow-Keras), Flask | UML 모델링 |
| 박근모 | 안드로이드 개발, 테스터| C, Java, Android, Python, HTML, CSS | UML 모델링 |

