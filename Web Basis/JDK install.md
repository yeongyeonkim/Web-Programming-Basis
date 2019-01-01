# <a href="https://www.edwith.org/boostcourse-web/lecture/16680/">JDK 설치 과정 [부스트코스]</a>

<h2>핵심개념</h2>

* JDK
* JRE

***

<h3>JRE</h3>

> JAVA언어를 작성된 프로그램을 실행하기 위해선 JRE(Java SE Runtime Environment)가 필요하다.<br>
JAVA언어를 사용하는 개발하자가 아닌 JAVA언어로 만들어진 프로그램을 실행하는 사용자라면 JRE만 설치한다.<br>
보통 JAVA를 설치한다는 것은 JRE를 설치하는 것을 말한다.<br>

<h3>JDK</h3>

> JAVA언어를 사용하는 개발자는 JAVA언어로 작성된 소스를 컴파일하고 관리할 필요가 있다.<br>
이때 사용되는 도구를 JDK(Java SE Development Kit)이라고 한다.<br>
컴파일한 결과를 실행하기 위해서 JDK안에는 JRE도 포함되어 있다.

<h3>JDK가 운영체제별로 설치파일을 제공하는 이유?</h3>

* JAVA파일은 운영체제에 독립적으로 작동하기 때문이다.<br>
.java파일로 작성된 자바파일이 .class파일로 컴파일되어 실행되는데, Windows든 Linux든 상관없이 실행된다.<br>
* 이렇게 운영체제에 상관없이 실행되는 것을 독립적이라고 이야기하는데, 이렇게 독립적으로 파일이 실행되기<br>
위해서는 실행되는 환경 즉, JRE가 제대로 갖춰져 있어야 하며, 이 때문에 JDK를 설치할 때 운영체제별로<br>
다르게 설치하는 것이다.
