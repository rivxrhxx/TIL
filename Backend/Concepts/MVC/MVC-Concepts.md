![[MVC.png]]
# **MVC(Model View Controller)**

데이터 및 논리 제어를 구현하는데 널리 사용되는 **소프트웨어 디자인 패턴**

사용자가 Controller을 조작하면 model을 통해서 데이터를 전달하고 그 정보를 바탕으로

시각적인 표현을 담당하는 View를 제어하여 사용자에게 전달됩니다.

1. 사용자가 Request(요청)를 Controller가 받는다
2. Controller는 Service에서 비즈니스로직을 처리한후 결과를 Model에 담는다
3. Model에 저장된 결과를 바탕으로 시각적 요소 출력 담당 View를 제어하여 사용자에게 전달

이 개념을 WEB에서 사용한다 생각하면

1. USER: 사용자가 웹사이트 접속
2. Manipulates : Controller는 사용자가 요청한 웹페이지를 보여주기위해 Model 호출
3. Updates : Model은 비즈니스 로직을 통해 DB및 파일과같은 데이터 제어후 결과반환 이후 Controller는 Model에게 반환받은 결과를 View에 반영
4. Sees: 데이터를 받아온 View가 사용자 웹사이트에 보여줌
[[View]][[Model]][[Controller]]