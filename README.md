
#include<iostream>
using namespace std;
//方法：比大小 找到适合位置 
int main()
{
    int N=0;
    cin>>N;
    int F[100]={0,1};
    int i=0;
    for(int i=2;i<100;i++)
    {
        F[i]=F[i-1]+F[i-2];
    }
    int result=0;
  for(int i=0;i<100;i++)
  {
      if(F[i]<=N&&F[i+1]>=N)
      {
          result=N-F[i]>F[i+1]-N?F[i+1]-N:N-F[i];
          cout<<result<<endl;
          break;
}
     
}
            
return 0;
}
