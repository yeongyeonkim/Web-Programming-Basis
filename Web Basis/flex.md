<h2><a href="http://flexboxfroggy.com/#ko">flex 실습 사이트</a></h2>

***

<h3>justify-content</h3>

* flex-start : 요소들을 컨테이너의 왼쪽으로 정렬.
* flex-end : 요소들을 컨테이너의 오른쪽으로 정렬.
* center : 요소들을 컨테이너의 카운데로 정렬.
* space-between : 요소들 사이에 동일한 간격을 둡니다.
* space-around : 요소들 주위에 동일한 간격을 둡니다.

***

<h3>align-items</h3>

* flex-start : 요소들을 컨테이너의 꼭대기로 정렬.
* flex-end : 요소들을 컨테이너의 바닥으로 정렬.
* center : 요소들을 컨테이너의 세로선 상의 가운데로 정렬.

※이때 개별 요소에 적용하고 싶다면 <b>align-self</b>를 사용한다.<br>align-items와 사용하는 값들은 같다.

***

<h3>flex-direction</h3>

* row : 가로로 정렬.
* row-reverse : 가로 역순정렬.
* column : 세로로 정렬.
* column-reverse : 세로 역순정렬.

***

<h3>flex-wrap</h3>

* nowrap : 모든 요소들을 한 줄에 정렬.
* wrap : 요소들을 여러 줄에 걸쳐 정렬.
* wrap-reverse : 요소들을 여러 줄에 걸쳐 반대로 정렬.

따로 설정해주지 않으면 한 획에서 요소들은 비좁게 자리를 차지하기 때문에<br>
그 획과 요소의 크기에 맞게 초과된 경우 다음 줄에서 정렬할 수 있도록 도와준다.

***

<h3>flex-flow</h3>

> flex-direction과 flex-wrap 두 속성의 값들을 인자로 받는다.

* row wrap : 가로로 요소들을 여러 줄에 걸쳐 정렬.
* column wrap : 세로로 요소들을 여러 줄에 걸쳐 정렬.

***

<h3>align-content</h3>

* flex-start : 여러 줄들을 컨테이너의 꼭대기에 정렬.
* flex-end : 여러 줄들을 컨테이너의 바닥에 정렬.
* center : 여러 줄들을 세로선 상의 가운데에 정렬.
* space-between : 여러 줄들 사이에 동일한 간격을 둡니다.
* space-around : 여러 줄들 주위에 동일한 간격을 둡니다.
