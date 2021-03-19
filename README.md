# cce0319

## 正課內容

```C
#include <stdio.h>
struct POINT{
    float x, y;
};
int main()
{
    struct POINT a ={4.1,3.2};
    printf("%f %f\n",a.x,a.y);

    a.x=1;
    a.y=2;
    printf("%f %f\n",a.x,a.y);
}
```

## 2
```C
#include <stdio.h>
struct DATA{
    int x,y;
    }a[3];
    struct DATA b={100,200};

    int main(){
        for (int i=0;i<3;i++){
            printf("a[%d]:%d %d\n",i,a[i].x,a[i].y);
        }
            printf("b: %d %d \n",b.x, b.y);
    struct DATA c;
    printf("c: %d %d 像亂碼\n",c.x, c.y);
    c=b;
    printf("c: %d %d \n",c.x, c.y);
    }
    ```
    
    ## 3
    ```C
    #include <stdio.h>
struct POINT {
    float x,y,z;
};
struct POINT point [5] ={{0,0,0},{1,0,0},{0,1,0},{1,1,1}};

int main ()
{
    struct POINT *p= & point[0];
    printf("%.2f %.2f %.2f\n",p->x,p->y,p->z);

    p++;
    printf("%.2f %.2f %.2f\n",p->x,p->y,p->z);

    p++;
    printf("%.2f %.2f %.2f\n",p->x,p->y,p->z);
}
```
## 基礎題：輸出從0到N的偶數 

```C
#include <stdio.h>
int main ()
{
	int n;
	scanf("%d",&n);
	for(int i=1;i<=n;i++){
	if(i%2==0)printf("%d ",i);
	}
}
```

## 基礎題：數字之首

```C
#include <stdio.h>
int main ()
{
	int n;
	scanf("%d",&n);
	if(n>=1000)
	printf("%d",n/1000);
	else if(n>=100)
	printf("%d",n/100);
	else if(n>=10)
	printf("%d",n/10);
	else if(n>=1)
	printf("%d",n/1);
	
	}
```
## 基礎題：字元判別
```C 
#include <stdio.h>
int main ()
{
	char n;
	scanf("%c",&n);
	
	if(n>='A'&&n<='Z')printf("U");
	else if(n>='a'&&n<='z')printf("L");
	else if(n>='0'&&n<='9')printf("D");
	else printf("O");
	}
```

## 基礎題：分開整數的每個數字
```C
#include <stdio.h>
int main ()
{
	int n;
	scanf("%d",&n);
	printf("%d   %d   %d   %d   %d",(n/10000)%10,(n/1000)%10,(n/100)%10,(n/10)%10,n%10);
	}
```
## 進階題：星星等腰三角 
 ```C
 #include <stdio.h>
int main()
{
	int n;
	scanf("%d",&n);
	for(int i=1;i<=n;i++)
	{	for(int j=1;j<=n-i;j++){
		printf(" ");
		}
	
	for(int k=1;k<=(i*2)-1;k++){
		printf("*");
		}
		printf("\n");
		}
		
	}
```
## 進階題：函數找整數的最大數字

```C
#include<iostream>
using namespace std;
int max_digit (int n)
{
	int max;
	max=n%10;
	while(n >0)
	{ if((n%10)>max) max = n%10;
	  n/=10;}
	  return max;
	  }
int main(){
  int n;cin>>n;
  cout<<"["<<max_digit(n)<<"]";
  return 0;
}
/* 上方C++ 的 main 函數 等價於 下方 C 的 main 函數
int main(void){
  int n;
  scanf("%d", &n);
  printf("[%d]", max_digit(n));
  return 0;
}
*/
```
## 進階題：擲骰統計 
```C
#include <stdio.h>
char a[999];
int main ()
{
	char count[7]={0};
	scanf("%s",&a);
	int i=0;
	while(a[i]!='\0')
	{
	count[a[i]-'0']++;
	i++;
	}
	for(i=1;i<=6;i++)
	{
	printf("%d:%d\n",i,count[i]);
	}
	}
```
##  進階題：除惡務盡

```C
#include <stdio.h>
int main ()
{
	char a[100];
	scanf("%s",&a);
	int i=0;
	while(a[i]!='\0')
	{
	if(a[i]!='2')
	printf("%c",a[i]);
	i++;
	}
	printf("\n");
	}
```
