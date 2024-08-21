## 1.	게임 설명 

Animal Pyter는 Python의 Pygame을 이용해 개발한 2인용 동물 격투 게임이다.
Pygame을 사용했음을 나타내기 위해 Pyter의 Py는 Pygame에서 유래했습니다.

![image](https://github.com/user-attachments/assets/17138e01-4d9c-4a8c-a0ad-8c49b973280b)

각 유저는 게임을 시작할 때 개인의 고유한 아이디를 입력한 후 게임을 플레이합니다. 게임이 종료되면 포인트는 아이디와 함께 저장됩니다.

![image](https://github.com/user-attachments/assets/de6b95c5-436a-490f-b634-b24c87d22c74)

게임을 통해 포인트를 쌓고, 그 포인트를 이용해 커스터마이징을 할 수 있습니다. 
유저들은 커스터마이징을 통해 무기의 색상을 바꿀 수도 있고 공격력을 높일 수도 있습니다.

![image](https://github.com/user-attachments/assets/87eb18bb-1ce5-42e5-9f69-5e011fb5f27f)

게임을 시작하면 유저들은 자신이 원하는 동물을 선택할 수 있습니다.
상대의 HP를 0으로 만들면 게임은 종료됩니다. 공격을 통해 MP를 획득하고 MP가 가득차면 필살기를 사용할 수 있습니다. 

![image](https://github.com/user-attachments/assets/3bd33ce3-2903-4d6b-b0f5-157008cb4355)

Animal Pyter는 여러가지 모드를 제공합니다. 이를 통해 지루하지 않게 게임을 플레이할 수 있습니다. 
게임은 한 판당 60초의 시간 제한이 있습니다. 시간이 끝날 때까지 승자가 나오지 않으면 시간 초과로 게임은 종료됩니다.   
5판 3선승 모드의 경우 시간 초과로 라운드가 종료되면 해당 라운드를 다시 시작합니다.
유저들의 편의성을 위해 옵션기능도 제공합니다. 언어 / 게임 배경 / 음량 조절 등이 가능하며 유저가 원하는 대로 Animal Pyter를 즐길 수 있습니다.

## 2.	조작 방법 설명
Animal Pyter는 키보드와 마우스 입력을 이용하여 플레이 합니다. 게임을 시작하면 키보드를 이용해 4자리의 영문 아이디를 입력합니다. 게임 메인 화면에서 원하는 버튼을 클릭하면 원하는 메뉴로 넘어갈 수 있습니다.
-	Player 1는 WASD 키를 이용해 이동을 하고 상단의 1, 2, 3 버튼을 이용해 공격을 합니다. 펀치 공격은 1, 무기 공격은 2, 필살기는 3 키를 사용합니다.
-	Player 2는 방향키를 이용해 이동을 하고 우측의 <, >, / 버튼을 이용해 공격을 합니다.펀치 공격은 <, 무기 공격은 >, 필살기는 / 키를 사용합니다.
-	
## 3.	구현 기능
-	캐릭터 구현 
Animal Pyter는 개, 여우, 고양이, 곰 4가지의 동물이 존재합니다. 유저는 게임을 시작 할 때 자신의 동물을 선택할 수 있습니다. 각각의 동물은 고유 특성을 반영하여 서로 다른 필살기, 스피드, 공격력을 가지고 있습니다. 예를 들어 곰은 다른 동물들에 비해 속도가 느리지만 강한 펀치 공격력을 가지고 있습니다. 게임 속 동물들이 걷거나 공격 자세를 취할 때마다 그에 맞는 이미지를 구현합니다. 또한 공격 / 방어 / 필살기를 사용할 때 마다 여러가지 효과음이 재생됩니다. 
-	사용자 정보처리
Animal Pyter는 아이디를 입력 받기 위해 TXT 파일을 이용합니다. 파일 처리를 통해 유저가 입력한 아이디가 파일 안에 존재하는지 확인하고, 만약 아이디가 파일에 있다면 저장된 포인트를 불러옵니다. 파일 안에 아이디가 없다면 입력한 아이디를 저장해 줍니다. 게임에서 승리하면 1판당 1000점의 포인트를 획득하고 이는 파일에 저장됩니다. 
-	커스터마이징 
저장된 포인트는 커스터마이징에 이용됩니다. 게임에서 승리하면 포인트가 쌓이고 일정 포인트 이상이 되면 포인트를 사용해 펀치나 무기의 바꾸거나 소량의 공격력을 추가할 수 있습니다. 커스터마이징을 할 때 마다 해당 포인트가 차감되고 그 포인트는 다시 파일에 저장됩니다.
-	옵션기능 
게임 안에서 옵션 기능 통해 배경음악, 효과음의 음량을 조절할 수 있습니다. 또한 언어를 영어 / 한국어 중에 선택할 수도 있습니다. 게임의 다채로움 높이기 위해 게임 배경화면을 도시 / 해변 / 우주 중 선택하여 플레이 할 수 있습니다. 게임 배경을 바꾸면 그에 맞게 배경음악도 바뀌어 재생됩니다.
-	모드 선택
Animal Pyter는 5판3선 모드 / 핸디캡 모드 / 무한 필살기 모드 / 연습 모드 를 제공합니다. 5판 3선승모드를 선택하면 3판을 먼저 승리한 유저가 승리합니다. 핸디캡 모드는 선택한 유저의 시작 HP가 30 감소한 상태로 시작합니다. 무한 필살기 모드는 시작부터 MP가 100으로 채워져 있고 필살기를 사용해도 감소하지 않습니다. 연습모드는 유저들이 연습을 할 수 있도록 만든 모드로 상대가 공격해도 HP가 닳지 않습니다.
