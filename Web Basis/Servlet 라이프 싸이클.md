<h3>라이프 사이클</h3>

* 어떤 객체의 생성부터 소멸까지의 과정

<h3>핵심 개념</h3>

* init
* service(request, response)
* destroy

```
public class LifecycleServlet extends HttpServlet {
	private static final long serialVersionUID = 1L;
    public LifecycleServlet() {
    	System.out.println("LifecycleServlet 생성!!");
    }
	public void init(ServletConfig config) throws ServletException {
		System.out.println("init test 호출!!");
	}
	public void destroy() {
		System.out.println("destroy 호출!!");
	}
	protected void service(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		System.out.println("service 호출!!");
	}
}
```

<img src="https://user-images.githubusercontent.com/45118806/50593847-8432e500-0edd-11e9-9866-2805a06727a1.PNG"></img>

***

1. 메모리에 존재하는 것을 판단하고 존재하지 않으면 객체를 생성하게 된다.<br>
존재하지 않는 지금, 생성자에 우리가 넣어준 메세지가 출력이 되는 것을 확인할 수 있다.

***

2. 한번 객체를 생성하고 메모리에 존재하게 된 뒤에는 새로고침 하면 service만 호출된다.<br>
서블릿은 서버에 서블릿 객체를 여러 개 만들지 않는다.<br>
요청 때 마다 매번 생성하는 일을 반복하는 것이 아니라<br>
요청 된 객체가 메모리에 있는지 없는지만 확인하고 있다면 service만 호출되는것.

***

3. destroy()는 언제 호출되는가? <br>
서블릿 수정하면 이미 메모리에 올라간 객체는 사용할 수 없기 떄문에 <br>
destroy가 호출되는 것을 볼 수 있다.

***

4. 그 후 새로고침 하면 메모리에 이제 존재하지 않기때문에<br>
다시 처음부터 객체를 생성하고 init호출하고 service를 호출을 수행하는 것을 볼 수 있다.

***
