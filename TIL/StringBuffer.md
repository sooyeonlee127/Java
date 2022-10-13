## **StringBuffer**

문자열을 추가하거나 변경할 때 사용하는 자료형

### append (문자열 생성)

**(1) StringBuffer, append 사용**

```
public class 클래스명 {
	public static void main(String[] args) {
			StringBuffer dream = new StringBuffer(); // StringBuffer 객체 dream 생
			dream.append("mark");
			dream.append(" ");
			dream.append("jeno");
			String result = dream.toString(); // String 자료형으로 변
			System.out.println(result); // mark jeno
	}
}
```

\- 객체 한번만 생성

\-  값이 생성된 후에 변경할 수 있다.

**(2) String 사용**

```
public class 클래스명 {
	public static void main(String[] args) {
			String result = "";
			result += "mark";
			result += " ";
			result += "jeno";
			System.out.println(result); // mark jeno
	}
}
```

\- 네 개의 객체 생성

\- 값이 생성된 후에는 변경할 수 없다

---

### insert (문자열 삽입)

**insert(삽입위치, 삽입할 문자열)**

```
public class 클래스명 {
	public static void main(String[] args) {
		StringBuffer j = new StringBuffer();
		j.append("jaemin jisung");
		j.insert(0, "jeno ");
		System.out.println(j.toString()); // jeno jaemin jisung
	}
}
```

---

### substring (문자열 중 특정 부분 뽑기)

**substring(시작위치, 끝위치)**

```
public class 클래스명 {
	public static void main(String[] args) {
		StringBuffer youth = new StringBuffer();
		youth.append("7llin' in our Youth");
		System.out.println(youth.substring(14, 19)); // Youth
	}
}
```