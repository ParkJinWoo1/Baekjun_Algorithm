# 문제 10952번 A + B -5

>## 문제
>
>두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.
>
>## 입력
>
>입력은 여러 개의 테스트 케이스로 이루어져 있다.
>
>각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10)
>
>입력의 마지막에는 0 두 개가 들어온다.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
		while(true) {	//무한루프
		int A = sc.nextInt();
		int B = sc.nextInt();
		
			if(A == 0 && B == 0) {	//입력받은 A와 B가 0이라면
				break;				//무한루프를 멈춘다
				
			}
			System.out.println(A+B);
		}
		
    }
}
```

---

# 문제 10951번 A + B -4

>## 문제
>
>두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.
>
>## 입력
>
>입력은 여러 개의 테스트 케이스로 이루어져 있다.
>
>각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10)

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
       Scanner sc = new Scanner(System.in);
		while(sc.hasNext()) {	//입력 받은 두 수마다 연산을 한다.
		int A = sc.nextInt();
		int B = sc.nextInt();
		
			
		System.out.println(A+B);
		}
    }
}
```

---

# 문제 1110번 더하기 사이클

> 0보다 크거나 같고, 99보다 작거나 같은 정수가 주어질 때 다음과 같은 연산을 할 수 있다. 먼저 주어진 수가 10보다 작다면 앞에 0을 붙여 두 자리 수로 만들고, 각 자리의 숫자를 더한다. 그 다음, 주어진 수의 가장 오른쪽 자리 수와 앞에서 구한 합의 가장 오른쪽 자리 수를 이어 붙이면 새로운 수를 만들 수 있다. 다음 예를 보자.
>
> 26부터 시작한다. 2+6 = 8이다. 새로운 수는 68이다. 6+8 = 14이다. 새로운 수는 84이다. 8+4 = 12이다. 새로운 수는 42이다. 4+2 = 6이다. 새로운 수는 26이다.
>
> 위의 예는 4번만에 원래 수로 돌아올 수 있다. 따라서 26의 사이클의 길이는 4이다.
>
> N이 주어졌을 때, N의 사이클의 길이를 구하는 프로그램을 작성하시오.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        
    	Scanner sc = new Scanner(System.in);
    	int N = sc.nextInt();	//ex> 26
    	
    	int num = N;
    	int cnt = 0;
    	
    	do {	//while의 조건을 실행하기 전 do{}문의 명령을 실행하고 진행한다.
    		num = num % 10 * 10 + (num / 10 + num % 10) % 10;
            //num = 26 %10 * 10 +(26 / 10 + 26 % 10) %10 =
            //		68 % 10 = 8
    		cnt ++;		//
    	}while(N != num) ;	//ex> 26이 다시 돌아올때까지 do문이 계속 돈다
    	
    	System.out.println(cnt);	//반복문이 돈 횟수를 출력
    }
}
```

