# [float 기반 샘플 화면 레이아웃 구성]

<img src="https://user-images.githubusercontent.com/45118806/50571874-c4b83300-0df7-11e9-800e-c77c6213f378.PNG"></img>

<h3>HTML</h3>

```
<header>부스트코스는 정말 유익합니다.
<div id="wrap">
  <nav class="left">
    <ul>
      <li>menu</li>
      <li>home</li>
      <li>name</li>
    </ul>
  </nav>
 <div class="right">
   <h2>
    <span>반가워요!</span>
     <div class="emoticon">:-)</div>
   </h2>
  <ul>
    <li>crong</li>
    <li>jk</li>
    <li>honux</li>
    <li>pobi</li>
  </ul>
 </div>
  <div class="realright">
    oh~ right
  </div>
</div>
<footer>코드스쿼드(주)</footer>
```

<h3>CSS</h3>

```
li {
  list-style:none;
}
header{
  background-color : #eee;
  
}
#wrap {
  overflow:auto;
  margin:20px 0px;
}
.left, .right, .realright {
  float:left;
  height: 200px;
  }
.left{
  width:17%;
  margin-right:3%;
  background-color : #47c;
}
.right {
  width:60%;
  text-align:center;
  background-color : #47c;
}
.realright{
  width:17%;
  margin-left:3%;
  background-color:#67c;
}
.right > h2 {
  position:relative;
}
.right .emoticon {
  position : absolute;
  top:0px;
  right:5%;
  color:#fff;
}
footer {
  background-color : #eee;
  clear:left;
}
```

left, right를 둘다 float:left 하면 메뉴들이 겹치게 된다.<br>
footer에 clear:left(both도 가능)를 써서 footer가 예상과 다른 결과가 나오는 것을 해결 가능.<p></p>

자식이 float인 경우엔 자신의 자식으로 인식하지 않기 때문에<br>
background-color가 제대로 적용이 되지 않을 수 있다.<br>
이때 <b>overflow:auto</b>를 사용해서 해결할 수 있다.
