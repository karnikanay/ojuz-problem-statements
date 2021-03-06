세상에서 가장 맛있는 과일이 사과라는 사실은 모두가 알고 있습니다. 이는 매우 당연해서 원숭이 Chris도 알고 있다고 하네요. 저 깊은 숲 속 강에는 사과 나무들이 빼곡히 자라 있습니다. 이 사과나무들에는 $1$번부터 시작해서 차례대로 연속하는 자연수 번호가 붙어 있습니다. 가끔 Chris는 숲 속에 들어와서, 연속하는 번호를 가진 사과나무들을 선택한 뒤 (구간 선택), 사과가 다 익은 나무가 몇 그루나 되는지 세어 봅니다. 가끔 연속하는 번호를 가진 사과나무들이 Chris가 오기 전에 모두 숙성되기도 합니다.

여러분은 Chris가 숲을 방문할 때마다 선택한 구간 내에서 숙성된 사과가 달린 나무가 몇 그루나 되는지 세어 보는 프로그램을 작성해야 합니다. 초기에 모든 사과들은 숙성되지 않았습니다.

### 입력 형식

첫 번째 줄에 이벤트의 수 $M$ ($1 \le M \le 100 000$)이 주어집니다. 다음 $M$개 줄에는 세 개의 정수 $D_{i}, X_{i}, Y_{i}$ ($1 \le D_{i} \le 2, X_{i} \le Y_{i}$)가 주어집니다. $D_{i} = 1$이라면, Chris가 숲 속으로 놀러 와서 숙성된 사과가 달린 나무를 세어 봅니다. $D_{i} = 2$라면, 구간에 속한 모든 나무들의 사과가 숙성됩니다. $X_{i}$와 $Y_{i}$는 각 이벤트에 필요한 구간을 나타냅니다.

구간을 계산할 때 추가로 고려해야 할 변수 $C$가 있습니다. 초기에 $C = 0$입니다. 각 이벤트에서 고려해야 할 구간은 $X_{i} + C$부터 $Y_{i} + C$까지입니다. $1 \le X_{i} + C, Y_{i} + C \le 10^{9}$임은 보장됩니다. 사과가 숙성되는 이벤트가 주어지면 $C$는 변하지 않습니다. 단 Chris가 숲 속에 놀러 오면, $C$는 Chris가 세어 낸 숙성된 사과가 달린 나무의 수로 변합니다.

주어지는 모든 구간은 닫힌 구간입니다.

### 출력 형식

Chris가 방문할 때마다 위에서 기술한 답을 한 줄에 하나씩 출력합니다.

### 예제

<table class='table table-bordered table-condensed'>
 <thead>
  <tr>
   <th style="width: 50%;">입력</th>
   <th style="width: 50%;">출력</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td class="code-font">3<br/>
2 5 8<br/>
2 7 10<br/>
1 1 10</td>
   <td class="code-font">6</td>
  </tr>
  <tr>
   <td class="code-font">4<br/>
2 2 3<br/>
1 1 3<br/>
2 2 3<br/>
1 -1 3</td>
   <td class="code-font">2<br/>
4</td>
  </tr>
  <tr>
   <td class="code-font">6<br/>
2 1 7<br/>
2 10 12<br/>
1 7 11<br/>
2 11 13<br/>
1 8 10<br/>
1 15 17</td>
   <td class="code-font">3<br/>
2<br/>
0</td>
  </tr>
 </tbody>
</table>


### 참고

35%의 데이터에 대해 $M \le 10 000, 1 \le X_{i} + C, Y_{i} + C \le 10^{6}.$

60%의 데이터에 대해 $1 \le X_{i} + C, Y_{i} + c \le 10^{7}.$