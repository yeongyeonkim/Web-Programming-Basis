<h2>[CSS를 HTML안에 선언하는 방식은 크게 3가지가 있다.]</h2>

1. inline
2. internal
3. external

<h3>inline</h3>
* 다른 CSS파일에 적용한 것 보다 가장 먼저 적용된다.

```
<p style="border:1px solid gray;color:red;font-size:2em;">
```

<h3>internal</h3>
* style 태그로 지정한다.
* 구조와 스타일이 섞이게 되므로 유지보수가 어렵다.
* 별도의 CSS 파일을 관리하지 않아도 된다.

```
<head>
<style>
p  {
  font-size : 2em;
  border:1px solid gray;
  color: red;
}
</style>
</head>

<body>
<div>...</div>
</body>
```

<h3>external</h3>
* 외부파일(.css)로 지정하는 방식이다.
* 가장 많이 사용하는 방법 중 하나로, 코드가 아주 짧지 않다면 가급적 이 방법을 사용한다.
* internal 코드와 같은 css코드를 구현하고, style.css와 같은 별도 파일로 만든다.

```
<html>
	<head>
		<link rel="stylesheet" href="style.css">
	</head>
	<body>
		<div>
			<p>
				<ul>
					<li></li>
					<li></li>
					<li></li>
					<li></li>
				</ul>
			</p>
		</div>
	</body>
</html>
```
