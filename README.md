1. 명령창에서 계산기를 구현하시오. 매개변수가 모자라면 프로그램을 종료하시오.
#include<stdio.h>
#include<stdlib.h>
int main(int n, char* v[]) {
int a, b, c;
printf("%d\n", n);
if (n < 4) {
printf("매개변수가 모자라요.\n");
exit(0);
}
a = atoi(v[1]);
b = atoi(v[3]);
switch (v[2][0]) {
case '+': c = a + b; break;
case '-': c = a - b; break;
default: break;
}
printf("%d\n", c);
}

2. my.txt 에 첫줄에 33 다음 줄에 22들어 있다. 이를 읽고 add() 함수를 이용하여 더하고 결과를 출력하시오. 반드시 오류에 대해 처리를 포함하시오.
#include<stdio.h>
#include<stdlib.h>
int add(int a, int b) {
 return a + b;
}
int main() {
 int a, b;
 FILE* fp = fopen("my.txt", "r");
 if (fp == NULL) { 
  puts("File not found!!");
  exit(0); 
 }
 fscanf(fp, "%d%d", &a, &b);
 fclose(fp);
 printf("%d\n", add(a, b));
}

3. 예상되는 문제를 하나 만들고, 코딩을 하시오.
ex) 애플, 키위, 바나나가 출력되게 하시오.
#include<stdio.h>
int main() {
char c1[6] = "apple";
printf("%s\n", c1);
char c2[5] = "kiwi";
printf("%s\n", c2);
char c3[7] = "banana";
printf("%s\n", c3);
}

4. 두명의 구조체 정보를 배열에 초기화하고 포인터로 화면에 출력하시오.
#include<stdio.h>
struct user {
 int a;
 char n[80];
} we[2] = { { 18,"jcshim" },{ 16,"jskim" } };
int main() {
 struct user* p;
 p = we;
 printf("%d %s\n", p->a, p->n);
 p++;
 printf("%d %s\n", p->a, p->n);
}
5. 두실수를 입력받아 면적계산하기
#include<stdio.h>
void main(){
 float width, height;
 float area;
 scanf("%f%f", &width, &height);
 area = width*height;
 printf("Area=%.2f\n", area);
} 
6. 실수하나를 반지름으로받아원의 면적구하기
#include <stdio.h>
void main(){
 float r, area;
 scanf("%f", &r);
 area = r*r*3.14;
 printf("%f", area);
} 
7. 두수중 큰수를 출력하시오
#include<stdio.h>
void main(){
	int a, b;
	while(1){
		printf("두값:");
		scanf("%d%d", &a, &b);
		if(a>b){
			printf("%d\n", a);
		}
		else{
			printf("%d\n", b);
		}
	}
}

8. 양수인지 음수인지 판단하는 프로그램
#include<stdio.h>
void main(){
	int a;
	while(1){
		printf("Enter Val:");
		scanf("%d",&a);
		if(a==0)     {printf("0입니다.\n");}
		else if(a>0) {printf("양수\n");}
		else         {printf("음수\n");}
	}
}

9. 학점 프로그램

#include<stdio.h>
void main()
{
	int kor;
	
	printf("국어성적<0~100>을 입력:");
	scanf("%d", &kor);
	
	if(kor >= 90)
	    printf("A학점\n");
	else if(kor >= 80)
	    printf("B학점\n");
	else if(kor >= 70)
	    printf("C학점\n");
	else if(kor >= 60)
	    printf("D학점\n");
	else   
	    printf("F학점\n");
}

10. 1~10 까지 출력하시오

#include<stdio.h>
void main(){
	int i;
	for(i=1;i<=10;i++){
		printf("%d\n", i);
	}
}

11. 두수를 더하는 함수

#include<stdio.h>
void add(int a, int b){
	int c = a+b;
	return(a+b);
}
void main(){
	int s, a=4, b=5;
	s = add(4,5);
	printf("%d\n", s);
}
 
 
 
#include<stdio.h>
void add(int a, int b){
	return(a+b);
}
void main(){
	int s = add(4,5);
	printf("%d\n", add(4,5));
}
 
 
 
#include<stdio.h>
int add(int a, int b){
	int c;
	c = a + b;
	return c; 
}
void main(){
	int e, d;
	scanf("%d%d", &e, &d);
	printf("%d", add(e, d));
	
}

12. 구조체 이름 나이 전번
#include<stdio.h>
struct user{
	int age;
	char n[80];
	char t[80]
};
void main(){
	int i;
	struct user we[3] ={{18, "phm", "010-9909-4999"}, {19, "kjy", "010-4592-6546"}, {20, "sjo", "010-2222-3333"}};
    printf("%d %s %s\n", we[0].age, we[0].n, we[0].t);
    printf("%d %s %s\n", we[1].age, we[1].n, we[1].t);
    printf("%d %s %s\n", we[2].age, we[2].n, we[2].t);
}




