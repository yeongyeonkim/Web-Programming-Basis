고유한 UI를 가지는 것은 <b>id</b>를 주고<br>
필요한 스타일, 같은 스타일을 적용할 일이 많다면 <b>class</b>

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
  
  <section id="nav-section">
    <nav>
      <ul>
        <li>Home</li>
        <li>Home</li>
        <li>About</li>
        <li>Map</li>
      </ul>
    </nav>
    
    <section id="roll-section">
      <div><img src="" alt=""></div>
      <div><img src="" alt=""></div>
      <div><img src="" alt=""></div>
    </section>
    
    <section>
      <ul>
        <li class="description">About us</li>
        <li class="description">
          <h3>What we do</h3>
          <div>Lorem ipsum dolor sit amet,</div>
        </li>
        <li class="description">Contact us</li>
      </ul>
    </section>

  </section>
  
  <footer><span>Copyright @codesquad</span></footer>
</body>
</html>
```
