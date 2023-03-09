#include<stdio.h>
void towers(int,char,char,char); //user defined function
int main()  
{
	int num;
	printf("Enter the no.of disks:"); 
	scanf("%d",&num);               //intake the number of towers
	printf("The size of moves involved\n");         //printing the number of moves the involved
	towers(num,'A','C','B');  //function call 
	return 0;
}

void towers(int num,char frompeg,char topeg,char auxpeg) 
{
	if(num==1) //in case one disk move it from frompeg to topeg
	{
		printf("\nmove disk 1 from peg %c to peg %c",frompeg,topeg);
		return;
	}
	towers(num-1,frompeg,auxpeg,topeg); //function call when num is not equal to 1
	printf("\nmove disk %d from peg %c to prg %c",num,frompeg,topeg);
	towers(num-1,auxpeg,topeg,frompeg);
}
