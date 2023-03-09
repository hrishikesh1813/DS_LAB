#include<stdio.h>
#include<ctype.h>
int stack[20];
int top=-1;
 
void push(int x)                //function to push the element
{
        stack[++top]=x;
}

int pop()
{
        return stack[top--];            //function to pop the elements
}

int main()
{
        char exp[20];
        char *e;
        int n1,n2,n3,num;
        printf("Enter the expression:\n");
        scanf("%s",exp);                //intaking the postfix expression
        e=exp;
        while(*e!='\0')                 //to check all the value in postfix expression
        {
                if(isalnum(*e))
                {
                        num=*e-48;         //if it is numerical pushing it into the stack    
                        push(num);
                }
                else
                {
                        n1=pop();
                        n2=pop();       //poping top two values when it encounters operator 
                        switch(*e)      //switch ladder for different operation
                        {
                                case '+':n3=n2+n1;
                                break;
                                case '-':n3=n2-n1;
                                break;
                                case '*':n3=n2*n1;
                                break;
                                case '/':n3=n2/n1;
                                break;
                                case '^':n3=n2^n1;
                                break;
                                
                        }
                
                push(n3);               //pushing the result into the stack top
                }
                e++;
        }
        printf("\n The result of postfix expression is:%d\n",n3);
        return 0;
}
