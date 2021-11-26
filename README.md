# FirstBoom
#include<stdio.h>
#include<process.h>

int stack[5],top=-1;
void push();
void pop();
void display();

void main()
{
    int choice;
    printf("enter 1 to push,2 to pop, 3 to show and 4 to exit: ");
    while (1)
    {
       printf("enter choice: ");
       scanf("%d",&choice);

       switch(choice)
       {
           case 1:
           push();
           break;
           case 2:
           pop();
           break;
           case 3:
           show();
           break;
           case 4:

           exit(0);
           break;
       }
    }
   getch(); 
}
void push()
{
    int item;
    if(top==5)
    {
        printf("\noverflow\n");
    }
    else
    {
        printf("put item to inserted: ");
        scanf("%d",&item);
        top=top+1;
        stack[top]=item;
    }
}
void pop()
{

    if (top==-1)
    printf("\nstack underflow\n");
    

else{
    printf("popped %d\n",stack[top]);
    top=top-1;
}
}
void show()
{
    printf("<---stack element are--->\n");
    for (int i = top; i >=0; i--)
    {
        printf("\t%d\n",stack[i]);
    }
    
}
