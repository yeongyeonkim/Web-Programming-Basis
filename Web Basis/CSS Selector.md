# [CSS Selector]

> HTML의 요소를 tag, id, html 태그 속성 등을 통해 쉽게 찾아주는 방법.

<h3>id를 사용한 예제</h3>

```
<style>
  #myspan {
    color : red;
  }
</style>

<span id="myspan">Hello World</span>
```

#을 사용한다. // 좀 더 구체적으로 하기 위해서 span#myspan 처럼 사용 가능

<h3>class를 사용한 예제</h3>

```
<style>
  .myspan {
    color : red;
  }
</style>

<span class="myspan">Hello World</span>
```

.을 사용한다.

<h3>그룹 선택</h3>

* 콤마(,)를 기준으로 여러 개를 지정 가능.

```
h1, span, div { color : red }
h1, span, div#id { color : red }
h1.span, div.classname { color : red }
```

* 하위 요소 선택(공백)

```
<style>
  #jisu span {
    color : red;
  }
</style>

<div id="jisu">
  <div>
    <span> red </span>
  </div>
  <span> red </span>  
</div>
```

* 자식 선택 (>)


```
<style>
  #jisu > span {
    color : red;
  }
</style>

<div id="jisu">
  <div>
    <span> black </span>
  </div>
  <span> red </span>  
</div>
```

* n번째 자식요소를 선택 (nth-child)

```
<style>
  #jisu > p:nth-child(2) {
    color : red;
  }
</style>

<div id="jisu">
  <h2>단락 선택</h2>
  <p>첫번째 단락</p>
  <p>두번째 단락</p>
  <p>세번째 단락</p>
  <p>네번째 단락</p>  
</div>
```

<img src="https://user-images.githubusercontent.com/45118806/50570319-ac312400-0dc9-11e9-98da-3ae3e80e0609.PNG"></img>
