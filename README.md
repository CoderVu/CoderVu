#include<stdio.h>
#include<math.h>
int main()
{
	int n,m;
	printf("Nhap bac phuong trinh ");
	scanf("%d",&n);
	float a[20],result,Amax;
	
		for(int i = 0 ; i <= n ; i++)
		{
			printf("a[%d] = ",i); scanf("%f", &a[i]);
		}
	
		for(int i = 0; i<=5;i++)
	    {
	        if(a[i] < 0){
	            m = i;
	            break;
	        }
	    }
		Amax = 0;
		for(int i = 0 ; i <= n ; i++)
		{
			if(a[i] < 0 && abs(a[i]) > Amax)
			{
				Amax = abs(a[i]);
			}
		}
		result = 1 + pow((Amax/a[0]),pow(m,-1));
		printf("%f",result);
}
