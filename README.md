-JAVA
썬에서 개발한 객체지향 프로그래밍언어
플랫폼에 독립적이다
클래스 라이브러리(JAVA API)를 기본적으로 제공한다
멀티쓰레드를 지원한다
동적 로딩을 지원한다

ㅇJVM = Java virtual machine
“자바를 실행하기 위한 가상기계” 
-> 자바는 다른 언어와는 다르게 JVM을 거쳐서 O/S를 가게 된다.
ㅇJDK = Java Development kit “자바 개발 도구”
ㅇJRE = Java Runtime Environment “자바 실행 환경”
-> 자바로 작성된 응용프로그램이 실행되기위한 최소환경

	 javac		     java.exe
Hello.java -> Hello.class -> 실행 
[소스 파일] 	[클래스파일]

-변수
->값을 저장할 수 있는 메모리상의 공간

기본형 :　실제값을 저장 
참조형 :  어떤값이 저장되어있는 주소를 값으로 정함

논리형 boolean
-> true, flase
문자형 char
-> 변수당 하나의 문자
정수형 byte, short, int, long
실수형 float, double


(Static)상수 = 값을 저장할 수 있는 공간이지만, 변수와달리 한번값을 저장하면 다른값으로 변경이 불가능하게된다. 선언과 동시에 초기화시켜야한다.
리터럴 = 상수와 구별하기위해서 상수를 다른이름으로 부르는 것,
	   즉 수학의 상수를 리터럴이라고 이야기한다.

문자형으로 넣을 때 char ch = ‘A’;이라면
문자가 저정되는 것 같지만 사실 문자의 유니코드 즉 숫자가 저장되게된다.

자동형변환 ? 경우에 따라 편의상의 이유로 형변환을 생략할수있는데,
컴파일러가 생략된 형변환을 자동적으로 추가해주는 것
-> 기존의 값을 최대한 보존할 수 있는 타입으로 자동 형변환한다.
-연산자
연산자- 연산을 수행하는 기호
피연산자- 연산자의 작업대상

산술연산자 + - * % / <<　>>
비교연산자 > < >= <= ==  !=
논리연산자 && || !
비트연산자 & | ^～
증감연산자 j＝++i; // 값이 참조되기전에 증가한다
	    j=i++;  // 값이 참조되고나서 증가한다
조건연산자 조건식 ? 식1:식2 
->조건식이 true일 때 식1로 가게되고, false일 때 식2로 가게된다

-조건문 반복문
ㅇif(조건식){
		}
ㅇif(조건식){
		} else {
			}
ㅇif(조건식){
}else if(){
	 }
 else if(){
	 }else{
		}
ㅇswitch(조건식){
		case 값:
		break;
		defalut:
			}
ㅇfor(초기화;조건식;증감식){
			}
->반복횟수를 알고있을경우에 적합하다.
ㅇwhile(조건식){
		}
ㅇdo{
	}while(조건식);

ㅇbreak; -> 자신이 포함된 가장 가까운 반복문을 벗어난다.
ㅇcontinue; -> 반복문의 끝으로 이동하며 다음 반복으로 
			넘어간다

-배열
ㅇ같은 타입의 여러변수를 하나의 묶음으로 다루는 것을 배열이라고한다.
int[] score = new int[5]; 
배열을 선언하는 것은 단지 생성된 배열을 다루기 위한 참조변수를 위한 공간이 만들어진다
int[] score; //배열 선언
배열을 생성해야만 비로소 값을 저장할 수 있는 공간이 만들어진다.
score = new int[5]; //배열을 생성

index는 배열의 요소마다 붙여진 일렬번호로 각 번호를 구별하는데 사용.
배열의 마지막 요소는 배열의 길이-1이다.
ㅇ배열의 길이 구하기 = 배열이름.length 
-> 이값은 상수이기 때문에 변하지 않는다. 
코드의 관리가 쉽고 에러가 발생할 확률이 적어진다.
int[] score = {50, 60, 70, 80, 90}
int[] score = new int[]{50, 60, 70, 80, 90}
배열을 초기화할수있는데, 초기화 할경우에는 위의 두경우다 가능하다.
int[] score = new int[5];
배열의 복사,  
1.for문을이용해서 배열복사.
2.System.arrycopy(num, 0, numNew, 0, num.length);
= num[0]에서 numNew[0]으로 num의 길이만큼

String[] name = new String[3];      -> String[] name = new String[3]; 
name[0] = new String(“Kim”);		name[0] = “Kim“
name[1] = new String(“Park”);		name[1] = “Park“
name[2] = new String(“Yi”);		name[2] = “Yi“

ㅇint num = Integer.parseInt(“123”) -> 변수 num에 숫자 123이 저장됨
//문자열을 숫자로 변환 해주는 메소드 Integer.parseInt(“”);

다차원 배열
int[][] score = new int[][];



-객체지향프로그래밍1
ㅇ객체지향언어
-실제 세계는 사물(객체)로 이루어져있으며, 발생하는 모든 사건들은 사물간의 상호작용이다.
-코드의 재사용성이 높고 유지보수가 용이하다.
-신뢰성이 높은 프로그래밍을 가능하게한다.

변수 = 속성
메소드 = 기능


ㅇ객체란?
-실제로 존재하는 것, 사물 또는 개념
ㅇ클래스
- 객체를 정의해놓은 것이며 객체를 생성하는데 사용된다.
  데이터와 데이터에 관련된 메서드의 집합
ㅇ인스턴스
-어떤클래스로부터 만들어진 객체를 클래스의 인스턴스라고한다.

ex) Tv t  -> 인스턴스를 참조하기 위한 변수를 만들어줄 수 있다.
	t = new Tv() -> 인스턴스를 생성할 수 있다.
	t.channel = 7 ; 인스턴스의 멤버변수의 값을 바꾸어줄 수 있다.

Tv t1 = new Tv();
Tv t2 = new Tv();
t1 = t2
t1에다가 t2가 가리키는 객체의 주소를 넣어주어서 t1이 t2를 가리키게 만들어준다.
그둘은 같은 객체를 가리키고있는것이며 t1이 가리키던 값은 가비지 컬렉션에 의해서
제거되게 된다.

ㅇ객체 배열 - 배열과 마찬가지로 객체를 배열로 나타내는 것
Tv[] tvArr = new Tv[3]; //참조변수 배열을 생성.
tvArr[0] = new Tv();
tvArr[1] = new Tv();
객체를 생성하고 난뒤에 배열의 각요소를 저장해주어야한다.
//제네릭 추가
//map hash arraylist 추가
변수
인스턴스변수
인스턴스마다 고유한상태를 유지해야하는 속성의 경우 인스턴스변수로 선언한다.
클래스변수
인스턴스 변수 앞에 static을 붙이기만 하면 클래스가 변수가 된다.
객체 생성없이 직접사용이 가능하다.
지역변수
메서드 내에 선언되어 메서드 내에서만 사용가능한 변수
메서드안에서 사용이 끝나면 소멸되어서 사용할수없게된다.
지역변수는 초기화해주지않으면 에러가 발생한다.

ㅇ메서드란?
-C언어의 함수와도 같은 의미이며 데이터와 멤버 변수에 대한 접근 권한을 갖는다.
어떤값을 입력하면 이 값으로 작업을 수행하여서 결과를 반환하게 된다.
메서드를 사용하면, 높은 재사용성과, 중복된 코드의 제거, 프로그램를 구조화할 수 있는 장점이있다.
반환타입 메서드이름 (매개변수명)
{
//메서드 호출시 수행되는 코드
}
만약 반환타입이 void가 아니라 반환값이 있는 경우 반드시 return문이 있어야한다.
반환값이있는데 return문이 없다면 에러가 발생하게된다.

ㅇJVM의 메모리구조
호출스택 = 메서드의 작업에 필요한 메모리 공간을 제공
힙 = 인스턴스변수들이 생성되는 공간

기본형 매개변수 ? 변수의 값을 읽기만 할 수 있다.
ex) void change(int x)
참조형 매개변수 ? 변수의 값을 읽고 변경할 수 있다.
ex) void change(Data d)

참조형 반환타입 ? 매개변수 뿐아니라 반환타입도 참조형이 될 수 있다.
		  메서드가 객체의 주소를 반환한다.

재귀 메서드 ? 메서드 내부에서 자기 자신을 호출하는 것

변수와 마찬가지로 메서드앞에 static이 붙어있으면 클래스메서드
		  		붙어있지 않으면 인스턴스 메서드.
메서드 내에서 인스턴스 변수를 사용하지 않으면, 
static을 붙이는 것을 고려하자
static을 붙인 메소드는 메소드 호출시간이 짧아지므로 성능이 향상된다.
클래스메소드는 인스턴스 변수를 사용할 수 없다.
클래스메소드에서는 인스턴스 메소드를 사용할 수 없다.

ㅇ오버로딩(overloading, 과적하다, 많이 싣다)
한 클래스내의 같은 이름의 메서드를 여러개 정의하는 것
메서드의 이름이 같아야하며, 매개변수개수나 타입이 달라야한다.
대표적인 오버로딩은 println메서드.

ㅇ생성자
생성자는 인스턴스가 생성될 때 호출되는 인스턴스 초기화 메서드이다.
생성자의 이름은 클래스의 이름과 같아야하며, 메서드와 구조가 비슷하지만, 리턴값이 없다.
Card(){ //매개변수가 없는 생성자
}
Card(String k, int num){ // 매개변수가 있는 생성자
}
클래스에 생성자를 정의하지않고도 인스턴스를 생성할수있었던 이유는
컴파일러가제공하는 ‘기본생성자’ 때문이다. 생성자가 하나도 정의 되지 않으면 자동적으로 컴파일러가 기본생성자를 추가해서 컴파일시켜준다.

-생성자에서 또 다른 생성자를 작성하기위해서는 첫 번째줄에서만 호출이가능하며,
-생성자의 이름으로 클래스이름대신 this를 사용하여야한다.
this(“white”, “auto” 4);

-객체지향프로그래밍2
ㅇ상속
-기존의 클래스를 재사용하여 새로운 클래스를 작성하는 것
적은양의 코드로 새로운 클래스를 작성할 수 있고, 공통적으로 코드를 관리하기 때문에 코드의 추가 및 변경이 매우 용이하다.
class Child extends Parent{
}
부모클래스가 변경되면 자식클래스는 자동적으로 영향을 받게되지만
자식클래스가 변경되면 부모클래스는 영향을 받지 않는다.

다른객체지향언어인 C++은 다중상속이 가능하지만, 
자바는 단일상속만을 허용한다.

ㅇ오버라이딩
부모클래스로부터 상속받은 메소드의 내용을 변경하는 것을 오버라이딩이라고한다. 상속은 메서드를 그대로 사용하기도하지만, 자손 클래스 자신에 맞게 변경해야 하는경우가 많다 
이름, 매개변수, 반환타입이 같아야한다.

오버로딩과 오버라이딩의 차이점
오버로딩 ? 기존에 없는 새로운 메소드를 정의하는 것
오버라이딩 ? 상속받은 메서드의 내용을 변경하는 것

super ? 조상의 멤버와 자신의 멤버를 구별하는데 사용하는 것
	  this와 사용하는 용도는 거의 같다. this와 마찬가지로 static 메서드
	  즉 클래스메서드에서는 사용할 수 없고, 인스턴스메서드에서만 사용	  이가능하다.
super() - 조상클래스의 생성자를 호출하는데 사용된다.

ㅇ패키지(package) 
클래스의 묶음인데, 클래스또는 인터페이스를 포함시킬수있으며 서로 관련있는것들을 묶을수있기 때문에 효율적으로 관리할 수 있다.
package 패키지명;

ㅇimport
컴파일러에게 소스파일에 사용된 클래스의 패키지에 대한 정보를 제공하는 것
ex)import java.utill.Calendar;
   import java.utill.*; 해주면 단순히 가능하다

ㅇ제어자
접근제어자 ? public, protected, default, private
다른 것   - static , final , abstract등등

static ? 클래스의, 공통적인 의미를 가지고있는 제어자
하나의 변수를 모든 인스턴스가 공유하게 된다.
클래스 변수. 인스턴스를 생성하지 않고도 사용이 가능하며, 모든 인스턴스에 공통적으로 사용되는 클래스변수가 된다.
클래스 메소드. 인스턴스를 생성하지 않고도 사용이 가능하며, 인스턴스멤버를 직접사용할 수 없다.

final ? 마지막의, 변경될 수 없는 의미를 가지고있으며, 
클래스-> 더 이상 확장할수없게되며, 다른 클래스의 조상이 될 수 없다.
메서드-> 더 이상 오버라이딩 할 수가 없게된다.
멤버변수, 지역변수-> 값을 변경할 수 없는 상수로 변경이된다.

abstract ? 클래스와, 메소드 둘다 미완성되게 만든다는 의미이다.
메소드의 선언부만 작성하고 구현하지않으며, 클래스에 사용되어 추상메소드가
존재한다는 것을 보여줄수가있다. 

public 전체
protected 자기클래스, 패키지, 자식
default 자기클래스, 패키지
private 자기클래스

ㅇ다형성 ? 부모클래스 타입의 참조변수로 자식클래스의 인스턴스를
참조할수있도록 하는 것
CaptionTv c = new CaptionTv();
Tv t = new CaptionTv();
참조변수    인스턴스
t는 부모클래스타입으로써 CaptionTv에 상속된 즉 Tv의 클래스의
변수나 메소드만 사용할수가있다.
참조변수의 타입이 부모클래스이고 인스턴스가 자식클래스는
사용이 가능하다.
다운캐스팅 ? 조상타입의 참조변수를 자손타입의 참조변수로 변환시키는 것
: 형변환 생략가능
업캐스팅 ? 자손타입의 참조변수를 조상타입의 참조변수로 변환시키는 것 
: 형변환 생략불가능
CaptionTv c = new CaptionTv();
Tv t = (Tv) c;



ㅇ인터페이스
구현된 것은 아무것도 없고 밑그림만 그려져있는 기본설계도.
자기혼자서 무엇을 하기보다는 다른 클래스를 도와주기 위해서 만들어졌다.
class 클래스이름 implements 인터페이스이름{
}
extends 말고 implements를 사용한다.

-예외처리
컴파일 에러 ? 컴파일 시에 발생하는 에러 
런타임 에러 ? 프로그램의 실행도중에 발생하는 에러
논리적 에러 ? 컴파일도 잘되고 실행도 잘되지만 의도한것과 다르게 동작하는 것을 의미한다. 

에러 ? 프로그램 코드에 의해서 수습될 수 없는 심각한 오류
예외 ? 프로그램 코드에 의해서 수습될 수 있는 다소 미약한 오류



예외가 발생하는경우
① 정수를 0으로 나눈 경우
② 배열의 첨자가 음수 또는 범위를 벗어나는 경우
③ 부적절한 형 변환이 일어나는 경우
④ 입출력을 위한 파일이 없는 경우 등등

try{
 	예외가 발생할 가능성있는 문장
}
catch(){
	예외의 종류에 따라 처리하는
}
finally{
	예외의 종류에 상관없이 무조건 처리되는 블록
}
-래퍼클래스
8개의 기본타입에 해당하는 데이터를 
객체로 포장해주는 클래스를 래퍼클래스라고한다
Interger Character 클래스만이 기본타입의 이름과 다르다.


//-쓰레드
동작하고 있는 프로그램을 프로세스(Process)라고 한다. 보통 한 개의 프로세스는 한 가지의 일을 하지만, 쓰레드를 이용하면 한 프로세스 내에서 두 가지 또는 그 이상의 일을 동시에 할 수 있게 된다. Thread는 직접 상속 받아 스레드 생성할수있으며, Runnable 인터페이스를 구현해서 생성할 수 있다.  run()메소드를 오버라이딩 해서 사용하면된다.
java.lang.Thread에서 제공이된다.
- 한번 종료한 스레드는 다시 시작시킬수 없다
- 스레드 객체를 다시 생성해야 한다.
- 한 스레드에서 다른 스레드를 강제 종료할 수 있다.
- 쓰레드 상태는 JVM에 의해 기록 관리된다.


ㅇ20181121
+ 해야할 것
get set
call by value
//비동기 동기
//람다식
*
framework 라이브러리 차이점//발표
mvc->mvvm,mvp//발표
*
arraylist, map, hash, stack, Queue
-제네릭
++ㅇ자료구조++ 
*
*코틀린 책빌려서 예습
(..........책을빨리빌리자)
3장전의 코틀린 문법 위주로 보자...
보자............................. 
예제... git hub에 올리자ㅋㅋㅋㅋㅋㅋ
//알고리즘
git hub...
*