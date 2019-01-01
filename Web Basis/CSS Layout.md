
<b>엘리먼트를 화면에 배치하는 것을 layout 작업이라고도하고,<br>
Rendering과정이라고도 한다.</b>

* display(block, inline, inline-block)
* position(static, absolute, relative, fixed)
* float(left, right)

<h3>display:block</h3>

<img src="https://user-images.githubusercontent.com/45118806/50570505-b6572080-0dd1-11e9-9abe-1e5fe39cd5c5.PNG"></img>

위 아래 어떤 설정도 하지 않았지만 아래로 흐르는 것을 알 수 있다.<br>
block 속성의 특징이라고 할 수 있다. (inline은 오른쪽으로 흐르게 할 수 있다.)

<h3>position</h3>

1. position 속성으로 특별한 배치를 할 수 있습니다.<br>
position 속성은 기본 static입니다. 

2. absolute는 기준점에 따라서 특별한 위치에 위치합니다.<br>
top / left / right / bottom 으로 설정합니다.<br>
기준점을 상위엘리먼트로 단계적으로 찾아가는데 static이 아닌 position이 기준점입니다.

3. relative는 원래 자신이 위치해야 할 곳을 기준으로 이동합니다.<br>
top / left / right / bottom로 설정합니다. 

4. fixed는 viewport(전체화면) 좌측, 맨 위를 기준으로 동작합니다.

<img src="https://user-images.githubusercontent.com/45118806/50570865-a0039180-0dde-11e9-839c-1aea12c5daa0.PNG"></img>

<h3>margin</h3>

위/아래/좌/우 엘리먼트와 본인간의 간격이다.

<h3>기본 배치에서 벗어나서 떠있기</h3>

<img src="https://user-images.githubusercontent.com/45118806/50570968-320c9980-0de1-11e9-8bd4-5f49d7dde703.PNG"></img>

.green에 float:left로 주었기 때문에 .red의 배치가 그 위로 보여지는 것을 확인할 수 있다.<br>
이 속성을 이용해서 .green의 속성이 width:100px 이고 .red의 속성이 100px이라면<br> 좌우로 나열된 그림을 볼 수 있는 것이다.

<h3>box-model</h3>
블록 엘리먼트의 경우 box의 크기와 간격에 관한 속성으로 배치를 추가 결정합니다<br>
margin, padding, border, outline으로 생성되는 것입니다.

<img src="https://user-images.githubusercontent.com/45118806/50571045-cfb49880-0de2-11e9-9e1d-e591401d6d96.PNG"></img>

<h3>엘리먼트 크기</h3>
block엘리먼트의 크기는 기본적으로 부모의 크기만큼을 가진다.<br>
예를들어 width:100%는 부모의 크기만큼을 다 갖는다.

<h3>box-sizing과 padding</h3>

box-sizing의 기본값은 content-box이다.<br>
이때 width의 값을 얼마를 주던 padding 같은 것으로 값을 늘려나갔을때 박스자체도 그것에 맞게 커지게 된다.<br>
이것을 원하지 않을 수 있기 때문에 content-box를 border-box로 설정해주면<br>
우리가 원하는 박스의 기본 크기를 고정한 채로 padding 따위의 속성을 유지하려고 할 것이다.

<img src="https://user-images.githubusercontent.com/45118806/50571080-a2b4b580-0de3-11e9-9178-4337745ddf5e.PNG"></img>

<h3>그래서, layout 구현 방법은?</h3>

* 전체 레이아웃은 float를 잘 사용해서 2단, 3단 컬럼 배치를 구현합니다.<br>
최근에는 css-grid나 flex 속성 등 layout을 위한 속성을 사용하기 시작했으며<br> 브라우저 지원범위를 확인해서 사용하도록 합니다.

* 특별한 위치에 배치하기 위해서는 position absolute를 사용하고,<br> 기준점을 relative로 설정합니다.

* 네비게이션과 같은 엘리먼트는 block 엘리먼트를 <br>inline-block으로 변경해서 가로로 배치하기도 합니다.

* 엘리먼트안의 텍스트의 간격과 다른 엘리먼트간의 간격은<br> padding과 margin 속성을 잘 활용해서 위치시킵니다.
