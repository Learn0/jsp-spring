# JSP로 단순한 스프링 기능 구현

---

## 설명
> v.1
> > 1. HttpServlet으로 *.do 값을 받아옴
> > 2. SAX파싱을 이용하여 XML에 등록한 패키지를 검색
> > 3. new File().listFiles를 이용하여 java파일 검색
> > 4. java파일 중 해당 패키지 내에서 isAnnotationPresent로 Controller(Annotation)이 등록된 클래스 확인
> > 5. 해당 클랙스 내에서 getAnnotation으로 RequestMapping(Annotation)이 등록된 메서드를 검색하여 값 일치 여부 확인
> > 6. invoke를 이용하여 일치한 메소드 실행
> > 7. RequestDispatcher로 request를 forward하여 전송 및 화면 출력

> v.2
> > 1. 톰캣에서 호출하기 위해 web.xml에 servlet을 등록(*.do 값을 받아와 특정 클래스를 실행하기 위함)
> > 2. SAX파싱을 이용하여 XML에 등록한 패키지를 검색
> > 3. new File().listFiles를 이용하여 class파일 검색
> > 4. class파일 중 해당 패키지 내에서 isAnnotationPresent로 Controller(Annotation)이 등록된 클래스 확인
> > 5. 해당 클랙스 내에서 getAnnotation으로 RequestMapping(Annotation)이 등록된 메서드를 검색하여 값 일치 여부 확인
> > 6. invoke를 이용하여 일치한 메소드 실행
> > 7. RequestDispatcher로 request를 forward하여 전송 및 화면 출력