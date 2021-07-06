# PATTERNS QUESTIONS


## 1
### Question
Input :
4
Output:
1
2*2
3*3*3
4*4*4*4
4*4*4*4
3*3*3
2*2
1

### Code

```
#include <iostream>
using namespace std;

int main() 
{
  int i,j,n;
  cin>>n;
  for(i=n;i<n+4;i++)
  {
    for(j=n;j<=i;j++)
    {
      cout<<i;
    }
    cout<<endl;
  }
  for(i=n+3;i>=n;i--)
  {
    for(j=n;j<=i;j++)
    {
      cout<<i;
    }
    cout<<endl;
  }
 }
```
<hr>

## 2
### Question
Input:
5

Output:
1
3*2
4*5*6
10*9*8*7
11*12*13*14*15



### Code

```
#include <iostream>
using namespace std;

int main() 
{
  int n,i,j,k=0;
  cin>>n;
  for (int i=1; i<=n; i++)
    {
        if (i%2 != 0)
        {
           for (j=k+1; j<k+i; j++)
                cout << j << "*";
            cout << j++ << endl;
            k = j;    
        }
       else
        {
           k = k+i-1;
             
            for (j=k; j>k-i+1; j--)
                cout << j << "*";
            cout << j << endl;    
        }
    }
}
```
<hr>

## 3
### Question
Input:
5

Output:
1 
2*2 
3*3*3 
4*4*4*4 
5*5*5*5*5 
5*5*5*5*5 
4*4*4*4 
3*3*3 
2*2 
1

### Code
```
#include <iostream>
using namespace std;
int main()
{
int i,j,k,N,count=0;
cin >> N;
for(i=1;i<=N;i++)
{
k=1;
for(j=0;j<i;j++)
{
cout << i;
if(k<i)
{
cout<<'*';
k=k+1;
}
}
cout << endl;
}
for(i=N;i>0;i--)
{
k=1;
for(j=0;j<i;j++)
{
cout << i;
if(k<i)
{
cout <<'*';
k=k+1;
}
}
cout << endl;
}
return 0;
}
```
<hr>

## 4
### Question
Input:
5

Output:
11112
32222
33334
54444
55556


### Code 
```
#include <iostream>
using namespace std;
int main() {
   int f=0;
  int n,i,j;
   cin>>n;
 int s=0;
  int l=n+1;
  int m,k;
   m=n;
 for(int i=1;i<=n;i++)
 {
  for(int j=2;j<l;j++)
   {
    if(i%2!=0)
       {
        cout<<i;
          k=i;
           f=1;
           s=j;
         if(s==m)
         {
          cout<<++k;
         }
       }
     if(i%2==0)
    {
      cout<<i;
       f=0;
     }
   }
   cout<<endl;
   if(i<n)
   {
    if(f==1)
     {
    cout<<++k;
    }
   }
 }
   return 0;
}
```

## 5
### Question
Input:
4

Output:

1*2*3*4*17*18*19*20 
--5*6*7*14*15*16
----8*9*12*13
------10*11

### Code
```
#include <iostream>

using namespace std;

int main()
{

	int num ;
  cin>>num;
	int space;

	int i, j, lterm, rterm;
	lterm = 1;
	rterm = num * num + 1;

	for (i = num; i > 0; i--) {
		for (space = num; space > i; space--)
			cout << "--";

		for (j = 1; j <= i; j++) {
			cout << lterm;
			cout << "*";
			lterm++;
		}
		for (j = 1; j <= i; j++) {
			cout << rterm;
			if (j < i)
				printf("*");
			rterm++;
		}

		rterm = rterm - (i - 1) * 2 - 1;
		cout << endl;
	}
}
```


