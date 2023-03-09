#include<stdio.h>  
#include<stdlib.h>  
struct node  
{  
    struct node *prev;  
    struct node *next;  
    int data;  		//creating the doubly linked node
};  
struct node *head;  
void insertion_beginning();  
void insertion_last();  
void insertion_specified();  
void deletion_beginning();  
void deletion_last();  
void deletion_specified();  
void display();  
void search();  		//user defined functions for each operation
void main ()  
{  
int choice =0;  
    while(choice != 9)  	//to get infinite loop till termination
    {  
        printf("\n*********Main Menu*********\n");  
        printf("\nChoose one option from the following list ...\n");  
        printf("\n===============================================\n");  
        printf("\n1.Insert in beginning\n2.Insert at last\n3.Insert at any random location\n4.Delete at beginning\n5.Delete from last \n6.Delete at random\n7.Search\n8.Display\n9.Exit\n ");  
        printf("\nEnter your choice:\n");  
        scanf("\n%d",&choice);  
        switch(choice)  
        {  
            case 1:  
            insertion_beginning();  
            break;  
            case 2:  
                    insertion_last();  
            break;  
            case 3:  
            insertion_specified();  
            break;  
            case 4:  
            deletion_beginning();  
            break;  
            case 5:  
            deletion_last();  
            break;  
            case 6:  
            deletion_specified();  
            break;  
            case 7:  
            search();  
            break;  
            case 8:  
            display();  		//function call for each operations
            break;  
            case 9:  
            exit(0);  
            break;  
            default:  
            printf("Please enter valid choice..");  
        }  
    }  
}  
void insertion_beginning()  		//function to insert data at beginning
{  
   struct node *ptr;   
   int item;  
   ptr = (struct node *)malloc(sizeof(struct node));  
   if(ptr == NULL)  
   {  
       printf("\nOVERFLOW");  
   }  
   else  
   {  
    printf("\nEnter Item value");  
    scanf("%d",&item);  
      ptr->data=item;		//insertng the element
   if(head==NULL)  
   {  
       ptr->next = NULL;  
       ptr->prev=NULL;  
       head=ptr;  		//creating the ll
   }  
   else   
   {  
        
       ptr->prev=NULL;  
       ptr->next = head;  
       head->prev=ptr;  
       head=ptr;  		//linking the new node to existing ll
   }  
   printf("\nNode inserted\n");  
}  
     
}  
void insertion_last()  		//function to insert node at the end of ll
{  
   struct node *ptr,*temp;  
   int item;  
   ptr = (struct node *) malloc(sizeof(struct node));  
   if(ptr == NULL)  
   {  
       printf("\nOVERFLOW");  
   }  
   else  
   {  
       printf("\nEnter value");  
       scanf("%d",&item);  
        ptr->data=item;  		//insertng the element
       if(head == NULL)  
       {  
           ptr->next = NULL;  
           ptr->prev = NULL;  
           head = ptr;  		//creating the ll
       }  
       else  
       {  
          temp = head;  
          while(temp->next!=NULL)  
          {  
              temp = temp->next;  
          }  
          temp->next = ptr;  
          ptr ->prev=temp;  
          ptr->next = NULL;  		//linking the new node to existing ll
          }  
             
       }  
     printf("\nnode inserted\n");  
    }  
void insertion_specified()  		//function to insert at random specified location in the node
{  
   struct node *ptr,*temp;  
   int item,loc,i;  
   ptr = (struct node *)malloc(sizeof(struct node));  
   if(ptr == NULL)  
   {  
       printf("\n OVERFLOW");  
   }  
   else  
   {  
       temp=head;  
       printf("Enter the location after which you want to insert:");  
       scanf("%d",&loc); 
       
       for(i=0;i<loc;i++)  
       {  
	   temp = temp->next;  
	   if(temp == NULL)  
	   {  
	       printf("\n There are less than %d elements", loc);  
	       return;  
	   }  
       } 
       
       printf("Enter value");  
       scanf("%d",&item);  
       ptr->data = item;  		//insertng the element
       ptr->next = temp->next;  
       ptr -> prev = temp;  
       temp->next = ptr;  
       temp->next->prev=ptr;  		//linking the new node to existing ll
       printf("\nnode inserted\n");  
   }  
}  
void deletion_beginning()  		//function to delete node at beginning
{  
    struct node *ptr;  
    if(head == NULL)  
    {  
        printf("\n UNDERFLOW");  
    }  
    else if(head->next == NULL)  
    {  
        head = NULL;   
        free(head);  		//deleting the node
        printf("\nnode deleted\n");  
    }  
    else  
    {  
        ptr = head;  
        head = head -> next;  
        head -> prev = NULL;  
        free(ptr);  		//deleting the node
        printf("\nnode deleted\n");  
    }  
  
}  
void deletion_last()  		//function to delete last node of ll
{  
    struct node *ptr;  
    if(head == NULL)  
    {  
        printf("\n UNDERFLOW");  
    }  
    else if(head->next == NULL)  
    {  
        head = NULL;   
        free(head);   		//deleting the node
        printf("\nnode deleted\n");  
    }  
    else   
    {  
        ptr = head;   
        while(ptr->next != NULL)  
        {  
            ptr = ptr -> next;   
        }  
        ptr -> prev -> next = NULL;   
        free(ptr);  		//deleting the node
        printf("\nnode deleted\n");  
    }  
}  
void deletion_specified()   	//deleting node at specified location
{  
    struct node *ptr, *temp;  
    int val;  
    printf("\n Enter the data after which the node is to be deleted : ");  
    scanf("%d", &val);  
    ptr = head;  
    while(ptr -> data != val)  
    	ptr = ptr -> next;  
    if(ptr -> next == NULL)  
    {  
        printf("\nCan't delete\n");  
    }  
    else if(ptr -> next -> next == NULL)  
    {  
        ptr ->next = NULL;  
    }  
    else  
    {   
        temp = ptr -> next;  
        ptr -> next = temp -> next;  
        temp -> next -> prev = ptr;  
        free(temp);  		//deleting the node
        printf("\nnode deleted\n");  
    }     
}  
void display()  //function to display all the elements in the ll
{  
    struct node *ptr;  
     
    ptr = head; 
    if(head==NULL)
    {
    	printf("\nUnderflow!!!!\n");
    }
    else
    { 
	    printf("\n printing values...\n"); 
	    while(ptr != NULL)  
	    {  
		printf("%d\n",ptr->data);  //displaying the ll elements
		ptr=ptr->next;  
	    }  
    }
}   
void search()  		//function to search the required element in LL
{  
    struct node *ptr;  
    int item,i=0,flag;  
    ptr = head;   
    if(ptr == NULL)  
    {  
        printf("\nEmpty List\n");  
    }  
    else  
    {   
        printf("\nEnter item which you want to search?\n");   
        scanf("%d",&item);  
        while (ptr!=NULL)  
        {  
            if(ptr->data == item)  
            {  
                printf("\nitem found at location %d ",i+1);  
                flag=0;  
                break;  
            }   
            else  
            {  
                flag=1;  
            }  
            i++;  
            ptr = ptr -> next;  
        }  
        if(flag==1)  
        {  
            printf("\nItem not found\n");  
        }  
    }     
          
}
