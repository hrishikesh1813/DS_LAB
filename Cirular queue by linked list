#include<stdio.h>
#include<stdlib.h>
struct node
{
	int data;
	struct node *next;
};
struct node *front=NULL;
struct node *rear=NULL;
void enqueue(int x)             //function to insert elements 
{
	struct node* newnode;
	newnode=(struct node*)malloc(sizeof(struct node));
	newnode->data=x;
	newnode->next=NULL;//0
	if(rear==NULL && front==NULL)
	{
		front=rear=newnode;
		rear->next=front;
	}
	else
	{
		rear->next=newnode;
		rear=newnode;           //inserting the element
		rear->next=front;
	}
}

void dequeue() //to delete an element from queue
{
	struct node* temp;
	temp=front;
	if(front==NULL && rear==NULL)
	{
		printf("Queue is empty\n");             //checking if queue is empty
	}
	else if(front==rear)
	{
		front=rear=NULL;
		free(temp);
	}
	else
	{
		front=front->next;
		rear->next=front;               //deletinf the element
		free(temp);
	}
}

void display() //to print the elements of queue
{
	struct node* temp;
	temp=front;
	if(front==NULL && rear==NULL)
	{
		printf("\nQueue is empty");
	}
	else
	{
		do
		{
			printf("\n%d",temp->data);              //printing all the values
			temp=temp->next;
		}while(temp!=front);
	}
}

int main() //main function
{
	int choice,n,i,data;
	
	do              //to get infinite loop till termination
	{
		printf("\n1.insertion\n2.deletion\n3.display\n4.exit\n");
		printf("enter your choice\n");
		scanf("%d",&choice);
		switch(choice)
		{
			case 1:
				printf("\nEnter the number of data:\n");
				scanf("%d",&n);
				printf("Enter your data:\n");
				i=0;
				while(i<n)
				{
					scanf("%d",&data);
					enqueue(data);
					i++;
				}
				break;
			case 3:
				display();
				break;
			case 2: dequeue();
				break;
			case 4: exit(0);                //function call for various operation 
			default:printf("\n invalid");
		}
	}while(choice!=0);
	return 0;
}
