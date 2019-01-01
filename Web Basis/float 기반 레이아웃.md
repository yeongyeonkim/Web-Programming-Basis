# [float 기반 샘플 화면 레이아웃 구성]

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

footer {
  background-color : #eee;
  clear:left;
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
```

<img src="https://user-images.githubusercontent.com/45118806/50571874-c4b83300-0df7-11e9-800e-c77c6213f378.PNG"></img>

