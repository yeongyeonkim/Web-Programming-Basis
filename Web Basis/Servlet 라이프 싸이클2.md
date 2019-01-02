# [Servlet 생명주기]

* WAS는 서블릿 요청을 받으면 해당 서블릿이 메모리에 있는지 확인합니다.
* if (메모리에 없음) {<br>
     -해당 서블릿 클래스를 메모리에 올림<br>
     -init() 메소드를 실행<br>
     }<br>
     -service()메소드를 실행
* was가 종료되거나, 웹 애플리케이션이 새롭게 갱신될 경우 destroy() 메소드가 실행됩니다.

<img src="https://user-images.githubusercontent.com/45118806/50596626-3a9bc780-0ee8-11e9-82ef-4f6d4184a1ee.PNG"></img>

***

<h3>service(request, response) 메소드</h3>
HttpServlet의 service메소드는 템플릿 메소드 패턴으로 구현합니다.

* 클라이언트의 요청이 GET일 경우에는 자신이 가지고 있는 doGet(request, response)메소드를 호출<br>
* 클라이언트의 요청이 Post일 경우에는 자신이 가지고 있는 doPost(request, reponse)를 호출

***

해당 서블릿에 URL주소를 직접 입력하거나 링크를 클릭하는 것은<br>
GET 방식으로 서버에게 요청을 보내게 되는 것이고<br>
이 경우 service()메서드가 호출이 되면서 해당 service()메서드는 자신의 doGet()메서드를 호출한다.
