##include <stdio.h>
#define N 100 
int main(){
	int n,k,m;
	scanf("%d %d %d",&n,&k,&m);
	int a[N]={0};
	int i,j;
	for(i=0;i<n;i++){
		a[i]=i=1;
	}
	i=k-1;
	while(n>1){
		i=(i+m-1)%n;
		for(j=i+1;j<n;j++){
		a[j-1]=a[j];	
		}
		n--;
		if(i==n){
			i=0;
		}
	}
	printf("%d\n",a[i]);
	return 0;
} 
