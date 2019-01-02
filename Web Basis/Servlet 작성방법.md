> 서블릿은 동적으로 응답 결과를 만들어내는 것이니까<br>
요청이 들어왔을 때 실행이 되면서 그때의 코드로 응답하게 하는 것.

```
protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
}
```

doGet을 보면 request, response가 있다.<br>
클라이언트가 요청할 때 서버는 요청을 받아내는 객체와 응답을 하기위한 객체<br>
두 개를 자동으로 만들어낸다.<p></p>

```
protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
  response.setContentType("text/html;charset=utf-8");
  PrintWriter out = response.getWriter();
}
```

우린 응답으로 1~10까지 출력하고 싶은 것이기 때문에 response를 사용한다.<br>
그리고 보낼 내용을 넣어줄 통로를 하나 얻어내야 한다. <br>
response객체 안의 매서드 getWriter()를 수행해서 PrintWriter 객체를 하나 얻어온다.<br>
out이라는 이름을 가진 통로를 만들게 되었고 이것으로 이제 출력을 한다.

```
protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
  response.setContentType("text/html;charset=utf-8");
  PrintWriter out = response.getWriter();
  out.println("<h1>1-10까지 출력!!</h1>");
  for(int i = 1;i <=10; i++)
  {
    out.println(i+"<br>");
  }
  out.close();
}
```

출력할 내용을 적고난 뒤 사용을 마친 객체 out을 close()해준다.<br>
그리고 실행시키면 원하는 결과의 웹이 보여진다.

* 코드에 보면 어노테이션으로 @WebServlet이라는 것이 만들어져있는 것을 볼 수 있다.<br>
그 안에 ("/something") 무언가가 들어있다.<br>
URL부분을 담당하는 것으로 내가 원하는 url주소를 설정하고 싶을때<br>
/ 뒤의 부분을 바꿔주면 된다.
