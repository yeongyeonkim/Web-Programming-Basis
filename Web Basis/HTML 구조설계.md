
div가 늘어나면 페이지 로드가 느려진다.<br>
의미없는 div를 줄이면 페이지 로드 시간이 줄어들고 버그 발생 가능성이 줄어든다.<p></p>

section 태그를 단순 컨테이너 용도로 사용하지 말고<br> 단순 그룹핑이면 div태그를 사용하는 게 좋다.

```
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
</head>
<body>
  <header>
    <h1>Company Name</h1>
    <img src=".." alt="logo">
  </header>
  
  <section>
    <nav>
      <ul>
        <li>Home</li>
        <li>Home</li>
        <li>About</li>
        <li>Map</li>
      </ul>
    </nav>
    
    <section>
      <div><img src="" alt=""></div>
      <div><img src="" alt=""></div>
      <div><img src="" alt=""></div>
    </section>
    
    <section>
      <ul>
        <li>About us</li>
        <li>
          <h3>What we do</h3>
          <div>Lorem ipsum dolor sit amet,</div>
        </li>
        <li>Contact us</li>
      </ul>
    </section>

  </section>
  
  <footer><span>Copyright @codesquad</span></footer>
</body>
</html>
```
