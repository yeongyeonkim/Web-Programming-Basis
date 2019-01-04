<img src="https://user-images.githubusercontent.com/45118806/50640889-937f6480-0fa9-11e9-8bd2-bbb16a0c3c48.png"></img>

<h3>요청과 응답</h3>

WAS는 웹 브라우저로부터 Servlet요청을 받으면,

* 요청할 때 가지고 있는 정보를 HttpServletRequest객체를 생성하여 저장합니다.
* 웹 브라우저에게 응답을 보낼 때 사용하기 위하여 HttpServletResponse객체를 생성합니다.
* 생성된 HttpServletRequest, HttpServletResponse 객체를 서블릿에게 전달합니다.

<h3>HttpServletRequest</h3>

* http프로토콜의 request정보를 서블릿에게 전달하기 위한 목적으로 사용합니다.
* 헤더정보, 파라미터, 쿠키, URI, URL 등의 정보를 읽어 들이는 메소드를 가지고 있습니다.
* Body의 Stream을 읽어 들이는 메소드를 가지고 있습니다.

<h3>HttpServletResponse</h3>

* WAS는 어떤 클라이언트가 요청을 보냈는지 알고 있고, 해당 클라이언트에게 응답을 보내기 위한<br>
HttpServletResponse객체를 생성하여 서블릿에게 전달합니다.
* 서블릿은 해당 객체를 이용하여 content type, 응답코드, 응답 메시지 등을 전송합니다.

***

<b>헤더</b>에 대한 정보를 알고 싶다.<br>
요청이 들어올 때 모든 정보들은 WAS가 HttpServletRequest라는 객체를 만들어서 담아주었는데<br>
그 담아둔 객체를 메서드 doGet(HttpServletRequest request, ~~ ) 처럼 request 파라미터로 가져왔다.<br>
그러므로 request에게 물어보면 된다. 따라서 request가 가지고 있는 메서드 중 getHeaderNames()라는 메서드가 있다.<br>
이 메서드는 모든 헤더 이름을 문자열 Enumertaion 객체로 반환해준다.

```
    protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		response.setContentType("text/html");
		PrintWriter out = response.getWriter();
		out.println("<html>");
		out.println("<head><title>form</title></head>");
		out.println("<body>");

		Enumeration<String> headerNames = request.getHeaderNames();
		while(headerNames.hasMoreElements()) {
			String headerName = headerNames.nextElement();
			String headerValue = request.getHeader(headerName);
			out.println(headerName + " : " + headerValue + " <br> ");
		}		
		
		out.println("</body>");
		out.println("</html>");
	}
```

