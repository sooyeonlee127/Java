숫자
Java의 숫자 자료형: 정수, 실수, 8진수, 16진수



1) 정수
- 종류: int, long, byte, short

- 기본값: int

int
: -2147483648 ~ 2147483647 범위의 수

long
: -9223372036854775808 ~ 9223372036854775807 범위의 수

- 접미사로 L을 붙여주어야 한다.







2) 실수
- 종류: float, double

- 기본값: double

float
: -3.4 * 10^38 ~ 3.4 * 10^38 범위의 수

- 접미사로 F를 붙여주어야 한다.

double
: -1.7 * 10^308 ~ 1.7 * 10^308 범위의 수




3) 8진수와 16진수
- int 자료형으로 표현한다.

8진수
: 숫자 0으로 시작 (ex 023;)

16진수
: 숫자0+알파벳x 로 시작 (ex 0xC;)





불(boolean)
: 참 또는 거짓의 값을 갖는 자료형



- 참(true), 거짓(false)만 대입될 수 있다.





문자(char)
: 한 개의 문자에 대한 자료형은 char를 이용한다.

char a1 = 'a';
- ' ' 로 감싸주어야 한다.



문자열(String)
(1) 리터럴 표기: 객체 생성 없이 고정된 값을 그대로 대입하는 방식

Stirng a = "NCT";
String b = "127";


(2) 새로운 String 객체를 생성하는 방식

String a = new String("NCT");
String b = new String("127");


문자열 내장 메소드
① equals

: 두개의 문자열이 동일한지를 비교하여 결과값을 리턴

String a = "NCT";
String b = "Dream";

System.out.println(a.equals(b)); // false




② indexOf

: 문자열에서 특정 문자가 시작되는 위치(인덱스)를 리턴

public class 클래스명 {
	public static void main(String[] args) {
		String a = "Favorite(Vampire)";
		System.out.println(a.indexOf("Vampire")); // 9
	}
}




③ contains

: 문자열에서 특정 문자열이 포함되어 있는지의 여부를 리턴

public class 클래스명 {
	public static void main(String[] args) {
		String a ="Baby Don't Like It";
		System.out.println(a.contains("Like")); // true
	}
}




④ charAt

: 문자열에서 특정 위치의 문자(char)를 리턴

public class 클래스명 {
	public static void main(String[] args) {
		String a = "Welcome To My Playground";
		System.out.println(a.charAt(5)); // m
	}
}


⑤ replaceAll

: 문자열 중 특정 문자열을 다른 문자열로 바꿈



public class 클래스명 {
	public static void main(String[] args) {
		String a = "NCT 2020";
		System.out.println(a.replaceAll("2020", "2022")); // NCT 2022
	}
}




⑥ substring

: 문자열 중 특정 부분을 뽑아낼 경우 사용

public class 클래스명 {
	public static void main(String[] args) {
		String a = "2 Baddies";
		System.out.println(a.substring(0, 3)); // 2 B
	}
}


⑦ toUpperCase

: 문자열을 모두 대문자로 변경할 때 사용

public class 클래스명 {
	public static void main(String[] args) {
		String a = "nct dream";
		System.out.println(a.toUpperCase()); // NCT DREAM
	}
}


⑧ split

: 문자열을 특정 구분자로 분리하는 메소드

String a = "무한적아;Limitless";
String[] result = a.split(";");


문자열 포매팅
String.format("문자열", 삽입할 값);



문자열 포맷 코드
%s: 문자열

%c: 문자 1개

%d: 정수

%f: 부동소수

%o: 8진수

%x: 16진수

%%: Literal% (%자체)







(1) 문자열 대입:  %s

// 문자열 대입
public class 클래스명 {
	public static void main(String[] args) {
		System.out.println(String.format("NCT %s", "DREAM")); // NCT DREAM
	}
}


(2) 숫자 대입: %d

// 숫자 대입
public class 클래스명 {
	public static void main(String[] args) {
		System.out.println(String.format("NCT %d", 127)); // NCT 127
	}
}


(3) 변수로 대입 + 2개 이상의 값 넣기

public class 클래스명 {
	public static void main(String[] args) {
		int number = 1;
		String name = "The Rainy Night";
		System.out.println(String.format("%s | Stick Together | EP. %d", name, number));
        		// The Rainy Night | Stick Together | EP. 1

	}
}




System.out.printf


String.format 메소드 사용(기존 방식)

System.out.println(String.format("NCT %s", "DREAM")); // NCT DREAM
: 포매팅된 문자열을 리턴





System.out.printf 메소드 사용

System.out.printf("NCT %s", "DREAM"); // NCT DREAM
: 포매팅된 문자열을 출력