# 문제 2557번 Hello World

>유틸 클래스를 사용하던 안하던, 유틸 클래스를 임포트 시킨 후
>
>클래스 명은 Main으로 통일!

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        System.out.println("Hello World!");
    }
}
```

---



# 문제 10718번 We love kriii

>별도 설명 없음.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        System.out.println("강한친구 대한육군");
        System.out.println("강한친구 대한육군");
    }
}
```

---

# 문제 10171번 고양이

>공백 및 위치를 예제 출력과 동일하게 출력해야 성공

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        System.out.println("\\    /\\");
        System.out.println(" )  ( ')");
        System.out.println("(  /  )");
        System.out.println(" \\(__)|");                 
    }
}
```

---

# 문제 10172번 개

>고양이문제와 마찬가지

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        System.out.println("|\\_/|");
        System.out.println("|q p|   /}");
        System.out.println("( 0 )\"\"\"\\");
        System.out.println("|\"^\"`    |");
        System.out.println("||_/=\\\\__|");                   
    }
}
```

---

# 문제 1000번 A + B

>Scanner 클래스를 이용하여 연산하기

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
	        int a = sc.nextInt();
	        int b = sc.nextInt();
	        
	        System.out.println(a+b);
    }
}
```

---

# 문제 1001번 A - B

>A + B 문제와 동일

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();
        int b = sc.nextInt();
        System.out.println(a-b);
    }
}
```

---

# 문제 10998번 A * B

>별도 설명 없음.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
        int a =sc.nextInt();
        int b = sc.nextInt();
         System.out.println(a*b);
    }
}
```

---

# 문제 1008번 A / B

>별도 설명 없음.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
          Scanner sc = new Scanner(System.in);
	        int a = sc.nextInt();
	        double b = sc.nextInt();
	        
	        System.out.println(a/b);
    }
}
```

---

# 문제 10869번 사칙연산

>사칙연산 문제

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
		int a = sc.nextInt();
		int b = sc.nextInt();

		System.out.println(a + b);
		System.out.println(a - b);
		System.out.println(a * b);
		System.out.println(a / b);
		System.out.println(a % b);
    }
}
```

---

# 문제 10430번 나머지

>예제 문제 풀기

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
		int a = sc.nextInt();
		int b = sc.nextInt();

		System.out.println(a + b);
		System.out.println(a - b);
		System.out.println(a * b);
		System.out.println(a / b);
		System.out.println(a % b);
    }
}
```

---

# 문제 2588번 곱셈

>(세 자리 수) × (세 자리 수)는 다음과 같은 과정을 통하여 이루어진다.
>
>![img](https://www.acmicpc.net/upload/images/f5NhGHVLM4Ix74DtJrwfC97KepPl27s%20(1).png)
>
>(1)과 (2)위치에 들어갈 세 자리 자연수가 주어질 때 (3), (4), (5), (6)위치에 들어갈 값을 구하는 프로그램을 작성하시오.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        		Scanner sc = new Scanner(System.in);
		int a = sc.nextInt();    //입력받을 수 첫번째 ex>472
		int b = sc.nextInt();    //입력받을 수 두번째 ex>385
	
	
		int v = b/100;        //ex> 385/100 = 3
                              //b의 100의자리
		int n = ((b/10) - (v*10));    //ex> (385/10) - (3*10) = 38-30 = 8
                                      //b의 10의자리
		int m = (b-(v*100) - (n*10));    // (385-(3*100) - (8*10))= 85 - 80 = 5
                                         // b의 1의 자리
		
		System.out.println(a*m);    //ex>472 * 5 = 2360 (3)
		System.out.println(a*n);    //ex>472 * 8 = 3776 (4)
		System.out.println(a*v);    //ex>472 * 3 = 1416 (5)
		System.out.println(a*b);    //ex>472 * 385 = 181720 (6)
    }
}
```

