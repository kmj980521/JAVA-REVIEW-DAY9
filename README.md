# JAVA-REVIEW-DAY9
자바 복습하기 9일차

1. 인스턴스 내부 클래스 - 인스턴스 변수를 선언할 때와 같은 위치에 선언하며, 외부 클래스 내부에서만 생성하여 사용하는 객체를 선얼할 때 사용, 다른 **외부 클래스에서 사용할 일이 없는 경우 내부 인스턴스 클래스로 정의**

인스턴스 내부 클래스는 외부 클래스가 먼저 생성되어야 사용할 수 있다. 그리고 인스턴스 **내부 클래스의 메서드는 외부 클래스의 메서드가 호출될 때 사용할 수 있다.**

2. 정적 내부 클래스 -**외부 클래스 생성과 무관**하게 사용할 수 있어야 하고, 정적 변수도 사용할 수 있어야 한다면 정적 내부 클래스를 사용, 내부 클래스가 static으로 선언이 되면 **외부 클래스의 변수는 static이 있는 정적 변수가 아닌 이상 접근이 안 됨**. 메인 클래스에서 외부클래스.내부클래스로 정적 내부 클래스 선언도 가능.

정적 내부 클레스에서 사용하는 메서드가 정적 메서드인 경우에는 외부 클래스와 정적 내부 클래스에 선언된 변수 중 **정적 변수만 사용 가능**

3. 지역 내부 클래스에서 사용하는 메서드의 지역 변수는 모두 상수로 바뀐다. 

```java
(int x,int y)->{return x+y}
```
이와같은 형식을 람다식이라고 한다. 함수형 프로그래밍이며, 함수 이름이 없는 익명 함수를 만드는 것이다. 람다식을 구현하기 위해 함수형 인터페이스를 만들고, 인터페이스에 람다식으로 구현할 메서드를 선언한다. 단, 사용하려는 클래스에서 implements해줄 필요는 없다.

람다식의 특징 1. 매개변수 자료형을 생략할 수도 있다. 2. 매개변수가 하나인 경우(두 개 이상인 경우에는 괄호 사용해야함)에는 괄호도 생략할 수 있다. 3.중괄호 안의 구현 부분이 한 문장인 경우 중괄호 생략 가능, 단 return문은 중괄호 생략이 불가능 . 4.중괄호 안의 구현 부분이 return문 하나라면 중괄호와 return을 모두 생략가능. 

람다식으로 구현하려면 **메서드를 하나만 포함하는 함수형 인터페이스만 가능하다**
