# PATTERNS QUESTIONS


## Half diamond pattern using numbers and star

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
