# 문제 2739번 구구단

>N을 입력받은 뒤, 구구단 N단을 출력하는 프로그램을 작성하시오. 출력 형식에 맞춰서 출력하면 된다.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
	Scanner sc = new Scanner(System.in);
		int N = sc.nextInt();
		
		
			for(int j = 1; j<10; j++) {		//j변수가 1부터 시작해서 10까지 갈 때 까지
                							//j에 +1씩 한다
				System.out.println(N+" * "+j+" = "+N*j);
                				//입력받은 N과 j를 곱한 값을 출력 (N단 출력)
			}
		
    }
}
```

---

# 문제 10950 A + B = 3

>두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        	Scanner sc = new Scanner(System.in);
	int T = sc.nextInt();	//T를 입력 받은 만큼 연산할 것이다
	
	for(int i = 0; i < T; i++) {	//i 변수가 0부터 입력받은 T만큼 연산할것이다
		int a=sc.nextInt();			//연산할 첫번째 수
		int j = sc.nextInt();		//연산할 두번째 수
		System.out.println((a+j));
	}

    }
}
```

---

# 문제 8393번 합

>n이 주어졌을 때, 1부터 n까지 합을 구하는 프로그램을 작성하시오.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        	Scanner sc = new Scanner(System.in);
	int n = sc.nextInt();	//입력받은 n 만큼 덧셈할거야
	int sum = 0;			//받은만큼 연산 할 수 있는 변수 설정
	
	for(int i = 1; i <= n; i++) {	//1부터 n만큼 +1씩
		
		sum += i;			//sum = sum + 1과 같은 말 sum에 + 1 한 값을 sum에 대입
	}

	System.out.println(sum);
    }
}
```

---

# 문제 15552번 빠른 A + B

>본격적으로 for문 문제를 풀기 전에 주의해야 할 점이 있다. 입출력 방식이 느리면 여러 줄을 입력받거나 출력할 때 시간초과가 날 수 있다는 점이다.
>
>C++을 사용하고 있고 `cin`/`cout`을 사용하고자 한다면, `cin.tie(NULL)`과 `sync_with_stdio(false)`를 둘 다 적용해 주고, `endl` 대신 개행문자(`\n`)를 쓰자. 단, 이렇게 하면 더 이상 `scanf`/`printf`/`puts`/`getchar`/`putchar` 등 C의 입출력 방식을 사용하면 안 된다.
>
>Java를 사용하고 있다면, `Scanner`와 `System.out.println` 대신 `BufferedReader`와 `BufferedWriter`를 사용할 수 있다. `BufferedWriter.flush`는 맨 마지막에 한 번만 하면 된다.
>
>Python을 사용하고 있다면, `input` 대신 `sys.stdin.readline`을 사용할 수 있다. 단, 이때는 맨 끝의 개행문자까지 같이 입력받기 때문에 문자열을 저장하고 싶을 경우 `.rstrip()`을 추가로 해 주는 것이 좋다.
>
>또한 입력과 출력 스트림은 별개이므로, 테스트케이스를 전부 입력받아서 저장한 뒤 전부 출력할 필요는 없다. 테스트케이스를 하나 받은 뒤 하나 출력해도 된다.
>
>자세한 설명 및 다른 언어의 경우는 [이 글](http://www.acmicpc.net/board/view/22716)에 설명되어 있다.
>
>[이 블로그 글](http://www.acmicpc.net/blog/view/55)에서 BOJ의 기타 여러 가지 팁을 볼 수 있다.

```java
import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.IOException;
import java.io.InputStreamReader;
import java.io.OutputStreamWriter;
import java.util.*;
public class Main{		//BufferedReader, BufferedWriter
    					//InputStreamReader, OutputStreamWriter
    					//위 함수들에 대해 공부해보자!!!
    					// Scanner함수보다 입력받아서 출력하는 과정 속도가 훨씬 짧다!?!
    public static void main(String[] args) throws IOException{
            BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out));
        int n = Integer.parseInt(br.readLine().trim());
        
        for (int i=0; i < n; i++) {
            String text = br.readLine();
            String[] word = text.split(" ");
            int a = Integer.parseInt(word[0]);
            int b = Integer.parseInt(word[1]);
            bw.write((a+b) + "\n");
        }
        
        bw.flush();
        bw.close();
    }
}
```

---

# 문제 2741번 N 찍기

>자연수 N이 주어졌을 때, 1부터 N까지 한 줄에 하나씩 출력하는 프로그램을 작성하시오.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        	Scanner sc = new Scanner(System.in);
	int n = sc.nextInt();	//입력받은 수 만큼 자연수 출력(내림차순)
	
	
	for(int i = 1; i <= n; i++) {	//ex> n이 3이라면
        							//1부터 3까지 1, 2, 3을 출력할거야
		
		System.out.println(i);
	}
    }
}
```

---

# 문제 2742번 기찍 N

>자연수 N이 주어졌을 때, N부터 1까지 한 줄에 하나씩 출력하는 프로그램을 작성하시오

```java
import java.util.*;
public class Main{
    //위와 같은 원리이지만 입력받은 수 만큼 오름차순으로 정렬하기
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
	int n = sc.nextInt();
	
	
	for(int i = n; i >= 1; i--) {
		
		System.out.println(i);
	}
    }
}
```

---

# 문제 11021번 A + B - 7

>두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
		int n = sc.nextInt();	//입력받은 수 만큼 출력문이 돌면서 
        						//돌아간 수와 연산을 출력해줄거야
		
        int cnt = 1;			//돌아간 수를 출력하기 위해 변수cnt 생성
		int sum = 0;			//연산을 위한 변수sum 생성
		for (int i = 0; i < n; i++) {	//n만큼 돌 때
			int x = sc.nextInt();		//연산 할 첫번째 수
			int y = sc.nextInt();		//연산 할 두번째 수
			sum = x + y;				//sum변수에 x + y 값 대입
			System.out.println("Case #" + cnt + ": " + sum);
            					//Case #cnt : sum 출력
			cnt++;				//돌때 마다 cnt에 +1씩 추가
    }
}
}
```

---

# 문제 11022번 A + B - 8

>두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        //위 문제와 동일한 원리, 연산하는 수까지 출력하는 문제!
       Scanner sc = new Scanner(System.in);
		int T = sc.nextInt();
		
		
		int cnt = 0;
		for(int i = 0 ; i < T ; i++) {
			int a = sc.nextInt();
			int b = sc.nextInt();
			cnt++;
			System.out.println("Case #"+cnt+": "+a+" + "+b+" = "+(a+b));
		}
    }
}
```

---

# 문제 2438번 별찍기 -1

>첫째 줄에는 별 1개, 둘째 줄에는 별 2개, N번째 줄에는 별 N개를 찍는 문제

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
       Scanner sc = new Scanner(System.in);
		
		int N = sc.nextInt();	//입력받은 줄까지 별 찍기
		
		if(1<=N && N<=100) {	//입력받은 수의 조건을 잡아줌
		for(int i = 1; i <= N ; i++) {	//줄을 표현하는 변수 i가
            							//1부터 N만큼 i에 +1씩
			for(int j = 1 ; j <= i ; j++) {		//별을 표시하는 행 변수 j가
                								//1 부터 i만큼 j에 +1씩
				System.out.print("*");			//별을 찍는다
			}
			System.out.println();				//행이 찍혀지고 enter를 하여 N만큼 실행
		}
		
		
		}	
    }
}
```

---

# 문제 2439번 별 찍기 -2

>첫째 줄에는 별 1개, 둘째 줄에는 별 2개, N번째 줄에는 별 N개를 찍는 문제
>
>하지만, 오른쪽을 기준으로 정렬한 별(예제 참고)을 출력하시오.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
		int N = sc.nextInt();	//입력받은 수 만큼 별찍기(오른쪽 정렬) ex>5
		
		
			for(int i = 0; i < N ; i++ ) {		//줄을 나타내는 변수 i 설정
				for(int j = 0; j < N-i-1; j++) { //공백을 나타내는 변수 j 설정
                    	//j가 0부터 5-0-1=4 ==4칸의 공백을 줌 " "
					System.out.print(" ");
				}for(int k = 0; k < 1+i; k++) {	//별을 나타내는 변수 k 설정
                    //4칸의 공백 후 별을 찍는다
					System.out.print("*");
				}
				System.out.println();
			}
    }
}
```

---

# 문제 10871번 X보다 작은 수

>정수 N개로 이루어진 수열 A와 정수 X가 주어진다. 이때, A에서 X보다 작은 수를 모두 출력하는 프로그램을 작성하시오.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
      Scanner sc = new Scanner(System.in);
		int N = sc.nextInt();	//N번만큼 정수를 입력받을거야
		int X = sc.nextInt();	//입력받은 수 중 X보다 작은수를 나타낼거기 때문에
        						//기준을 나타낼 정수 X 변수 출력
		
		int arr [] = new int[N];	//arr변수에 N번만큼 index가 정해질 정수형 배열 선언
		
	for(int i = 0; i < N; i++) {	
		arr[i] = sc.nextInt();		//배열을 N번지만큼 받을거야 scanner로
	}
		sc.close();					//받은 다음
	for(int i = 0; i < N; i++) {	//N만큼
		if(arr[i] < X) {			//정해준 X정수 보다 작다면
			System.out.print(arr[i]+ " ");	//그애들을 출력해줄거야
		}
	}
    }
}
```

---