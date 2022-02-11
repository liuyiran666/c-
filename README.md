# c self-learning
#include <stdio.h>
int main()
{
	int x ;
	int i=1;
	scanf("%d",&x);
	int t = x ;
	while (x>0){
		x=x/10;
		i=i+1;
	}
	//计算位数  i-1 是位数   
	/* 12345 / 10000=1
	   12345 % 10000=2345
	   2345 / 1000 = 2
	   2345 % 1000 =345 */
	   
	int mask = pow(10,i-2); /* 10的 i-2次方  也就是 位数-1 次方 */ 
	int d;       
	                
	while (i!=1){
		d = t/mask;
		t = t%mask;
		printf ("%d",d);
		if (i!=2){
			printf(" ");
		}
		mask=mask/10;
		i=i-1;
	} 
	// 位数 不是 0 的时候 进入循环    位数 不是 最后一位 时候打空格 每次除完得到第一位 就得位数减一 t也得变 
	return 0;
}
