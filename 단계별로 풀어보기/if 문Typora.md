# 문제 1330번 두 수 비교하기

>두 정수 A와 B가 주어졌을 때, A와 B를 비교하는 프로그램을 작성하시오.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
		int a = sc.nextInt();
		int b = sc.nextInt();
		
		if(a>b) {	//a가 b보다 크다면
			System.out.println(">");	//a가 크다는 표시 출력
		}else if(a<b) {		//a가 b보다 작다면
			System.out.println("<");	//b가 크다는 표시 출력
		}else {
			System.out.println("==");	//둘과 다른 조건인 a와 b가 같다면
            							//같다는 표시 출력
		}
	
    }
}
```

---

# 문제 9498번 시험 성적

>시험 점수를 입력받아 90 ~ 100점은 A, 80 ~ 89점은 B, 70 ~ 79점은 C, 60 ~ 69점은 D, 나머지 점수는 F를 출력하는 프로그램을 작성하시오.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);
		int score = sc.nextInt();
		//if문으로 사용할 수 있지만 쓰기 더 쉽고 가독성 좋은 switch문을 이용했다.
		switch(score/10) {	//score를 10으로 나눈값으로 조건을 둔다
		case 10:	//score가 10점 이라면(10으로 나누어서 나온 값!)
		case 9:		//score가 9점 이라면
			System.out.println("A");	//A를 출력 후 switch문 종료
			break;
		case 8:
			System.out.println("B");
			break;
		case 7:
			System.out.println("C");
			break;
		case 6:
			System.out.println("D");
			break;
			default :
				System.out.println("F");
				break;
		}
    }
}
```

---

# 문제 2753번 윤년

>연도가 주어졌을 때, 윤년이면 1, 아니면 0을 출력하는 프로그램을 작성하시오.
>
>윤년은 연도가 4의 배수이면서, 100의 배수가 아닐 때 또는 400의 배수일 때이다.
>
>예를 들어, 2012년은 4의 배수이면서 100의 배수가 아니라서 윤년이다. 1900년은 100의 배수이고 400의 배수는 아니기 때문에 윤년이 아니다. 하지만, 2000년은 400의 배수이기 때문에 윤년이다.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        	Scanner sc = new Scanner(System.in);
		int year = sc.nextInt();
	
		if(year %4 == 0 && year %100 != 0 ||year % 400 ==0) {
            //주어진 year가 4로 나누어 떨어지거나 100으로 나누어 떨어지지 않으면,
            //또한 400으로 나누어 떨어진다면 
			System.out.println("1");	//1을 출력
		}else {
			System.out.println("0");	//그렇지 않으면 0을 출력한다
		}
	
    }
}
```

---

# 문제 14681번 사분면 고르기

>흔한 수학 문제 중 하나는 주어진 점이 어느 사분면에 속하는지 알아내는 것이다. 사분면은 아래 그림처럼 1부터 4까지 번호를 갖는다. "Quadrant n"은 "제n사분면"이라는 뜻이다.
>
>![img](https://onlinejudgeimages.s3-ap-northeast-1.amazonaws.com/problem/14681/1.png)
>
>예를 들어, 좌표가 (12, 5)인 점 A는 x좌표와 y좌표가 모두 양수이므로 제1사분면에 속한다. 점 B는 x좌표가 음수이고 y좌표가 양수이므로 제2사분면에 속한다.
>
>점의 좌표를 입력받아 그 점이 어느 사분면에 속하는지 알아내는 프로그램을 작성하시오. 단, x좌표와 y좌표는 모두 양수나 음수라고 가정한다.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        	Scanner sc = new Scanner(System.in);
		int x = sc.nextInt();
		int y = sc.nextInt();
		
		if(x>0 && y>0) {	//x와 y가 0보다 크다면
			System.out.println("1");	//1사분면에 위치
		}else if (x<0 && y>0) {		//x가 0보다 작고 y가 0보다 크다면
			System.out.println("2");	//2사분면에 위치
		}else if (x<0 && y<0) {		//x와 y가 0보다 작다면
			System.out.println("3");	//3사분면에 위치
		}else {						//그렇지 않다면(x가 0보다 크고 y가 0보다 작다면)
			System.out.println("4");	//4사분면에 위치
		}
    }
}
```

---

# 문제 2884번 알람 시계

>상근이는 매일 아침 알람을 듣고 일어난다. 알람을 듣고 바로 일어나면 다행이겠지만, 항상 조금만 더 자려는 마음 때문에 매일 학교를 지각하고 있다.
>
>상근이는 모든 방법을 동원해보았지만, 조금만 더 자려는 마음은 그 어떤 것도 없앨 수가 없었다.
>
>이런 상근이를 불쌍하게 보던, 창영이는 자신이 사용하는 방법을 추천해 주었다.
>
>바로 "45분 일찍 알람 설정하기"이다.
>
>이 방법은 단순하다. 원래 설정되어 있는 알람을 45분 앞서는 시간으로 바꾸는 것이다. 어차피 알람 소리를 들으면, 알람을 끄고 조금 더 잘 것이기 때문이다. 이 방법을 사용하면, 매일 아침 더 잤다는 기분을 느낄 수 있고, 학교도 지각하지 않게 된다.
>
>현재 상근이가 설정한 알람 시각이 주어졌을 때, 창영이의 방법을 사용한다면, 이를 언제로 고쳐야 하는지 구하는 프로그램을 작성하시오.

```java
import java.util.*;
public class Main{
    public static void main(String[] args){
        	Scanner sc = new Scanner(System.in);

		String x = sc.next();	//시간을 나타낼 변수
		String y = sc.next();	//분을 나타낼 변수
		
		int a = Integer.parseInt(x);	//String을 int형으로 형 변환
		int b = Integer.parseInt(y);	//위와 동일
		
		b = b-45;	//분을 나타낼때 45분 일찍을 나타내기 위해 
        			//변수 b에 45를 뺀다
		if(b > 60) {	//b가 60보다 작다면(시간이 늘어남)
			a +=1;		//시간에 1을 더해주고
			b = b-60;	//b에서 60을 뺀다
		}else if(a > 23) {	//a가 23보다 크다면 (24시가 넘어가는 상황에 조건)
			a = a-24;	//a에 24를 뺀다
			
		}else if(b < 0) {	//b가 0보다 작다면(시간이 줄어듬)
			b = b+60;		//b에 60을 더함
			a -= 1;			// 시간을 1 빼줌
			 if (a < 0) {	//이때 a가 0보다 작다면 (24시를 0으로 표현)
				a = 23;		//시간을 23시로 표현
			}
		}
		System.out.println(""+a+" "+b);
    }
}
```

---

