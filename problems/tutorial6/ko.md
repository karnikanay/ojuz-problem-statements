지학이는 그의 친구들 5명과 함께 퀴즈쇼에 나갔습니다.

퀴즈쇼의 사회자인 승현이는, 지학이가 매우 똑똑하다는 것을 알고 있어 굉장히 어려운 문제를 냈습니다.

그 문제는 다음과 같습니다.

먼저, 지학이의 친구들 5명에게 0 이상 9 이하의 정수가 적힌 모자를 씌워 방 안에 들어가도록 합니다.

지학이의 친구들은 다른 친구들의 모자에 적힌 수를 볼 수는 있지만, 자신의 모자에 적힌 수를 볼 수는 없습니다.

지학이는 외부에서 5명의 모자에 적힌 수를 보고, 5명 중 한 명을 지목하고 붉은색과 푸른색 카드 중 하나를 골라 승현이에게 전달하게 할 수 있습니다.

어떤 색의 카드가 누구에게 전달되는지는 방 안에 있는 5명 모두가 볼 수 있습니다.

카드를 50장 이하로 보내서 방 안에 있는 5명의 친구들에게 승현이가 랜덤한 순서로 질문을 해서, 모두 자신의 모자에 적힌 수를 맞힐 경우 지학이와 친구들 모두 상금을 받을 수 있습니다.

단, 전달하는 카드의 수가 적을수록 더 많은 상금을 받기 때문에, 최대한 전달하는 카드의 수를 줄여야 합니다.

### 할 일

두 개의 함수 jeehak 과 friends 를 작성하세요. jeehak 은 외부에서 카드를 보내는 지학이를 대신하는 함수이고, friends 는 지학이가 보낸 카드와 다른 친구들의 모자에 적힌 수를 보고 자신의 모자에 적힌 수를 추측하는 친구를 대신하는 함수입니다.

* void jeehak(int A[])
 - **A** : 5개의 정수로 이루어진 1차원 배열입니다. 5명의 모자에 적힌 수가 순서대로 주어집니다. 인덱스는 1부터 5까지입니다.
 카드를 보낼 때는 send(int X,int Y) 함수를 호출하여 보냅니다. X는 카드를 받을 친구의 번호이고, Y는 카드의 색으로 0은 붉은색, 1은 푸른색을 뜻합니다. ( 1 ≤ X ≤ 5 , 0 ≤ Y ≤ 1 )
 
* void friends(int A[],int N,int X[],int Y[])
 - **A** : 5개의 정수로 이루어진 1차원 배열입니다. 5명의 모자에 적힌 수가 순서대로 주어집니다. 자신의 모자는 -1이 적힌 것으로 들어옵니다. 인덱스는 1부터 5까지입니다.
 - **N** : 지학이가 보낸 카드의 수를 뜻합니다.
 - **X**,**Y** : 지학이가 보낸 카드를 받은 친구의 번호와 색이 순서대로 주어집니다. 인덱스는 1부터 N까지입니다. ( 1 ≤ X[i] ≤ 5 , 0 ≤ Y[i] ≤ 1 )
 자신의 모자에 적힌 수를 guess(int A) 함수를 호출하여 추측합니다. A는 자신의 모자에 적힌 수를 뜻합니다. ( 0 ≤ A ≤ 9 )
 
### 서브태스크

#### 서브태스크 1 (20점)

* 지학이가 보낸 최대 카드는 50개 이하여야 합니다.

#### 서브태스크 2 (최대 80점)

* 지학이가 보낸 최대 카드의 수를 $ N $ 이라고 할 때, 점수는 $ max ( 0 , 80 \times ( 1 - log_{50} N ) ) $ 점입니다.

### 구현 시 유의사항

#### 채점 환경

* 프로그램의 최대 실행 시간은 1초입니다. 채점 프로그램의 실행 시간이 0.3초를 넘지 않음이 보장되어 있습니다.
* 메모리 제한은 64MB이며, 스택 메모리 역시 전체 메모리에 포함됩니다.

#### 인터페이스

<u><strong><a href="https://s3.ap-northeast-2.amazonaws.com/oj.uz/old/tutorial6/grader.zip">여기</a></strong></u>를 클릭하시면 개발에 필요한 인터페이스가 제공됩니다. 이를 이용해서 이 문제를 좀 더 쉽게 해결할 수 있을 것입니다. 아래에 그 설명이 있습니다.

* 작성해야 할 파일: jeehak.c 와 friends.c 또는 jeehak.cpp 와 friends.cpp
* 채점 프로그램 인터페이스: jeehak.h 와 friends.h
* 견본 채점 프로그램: grader.c 또는 grader.cpp
* 입출력 예제: example.in 과 example.out

여러분은 jeehak.c 와 friends.c 또는 jeehak.cpp 와 friends.cpp 를 작성하신 후 이 내용을 복사해서 제출하시면 됩니다. 단, jeehak.c 또는 jeehak.cpp 파일의 상단에 있는 #include"jeehak.h" 또는 friends.c 또는 friends.cpp 파일의 상단에 있는 #include"friends.h" 를 지우고 작성하시면 컴파일 에러가 발생하거나 프로그램이 올바른 답을 내지 못하여 점수를 받을 수 없습니다.