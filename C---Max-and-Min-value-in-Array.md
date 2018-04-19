#include <stdio.h>
#include <conio.h>

int main() {
	int n;
	printf("Please input a number: ");
	scanf("%d", &n);
	
	int a[n];
	for (int i=0; i<n; i++){
		printf("Please input a[%d]: ", i);
		scanf("%d", &a[i]);
	}
	
	for (int j=0; j<n; j++){
		printf("a[%d] = %d\n", j, a[j]);
	}

	int temp;
	for (int k=0; k<n-1; k++){
		for (int m=k+1; m<n; m++){
			if (a[k] > a[m]){
				temp = a[k];
				a[k] = a[m];
				a[m] = temp;		
			}
		}
	}
	printf("\n");
	for (int j=0; j<n; j++){
		printf("a[%d] = %d\n", j, a[j]);
	}
	printf("\nMin and Max value of a array are %d and %d.", a[0], a[n-1]);
}
