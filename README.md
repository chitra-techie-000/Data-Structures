# Data-Structures
#include <stdio.h>
#include <conio.h>
#define SIZE 10
int stack[SIZE], top=-1;
void push(int value){
    if(top==SIZE){
        printf("\nStack is Full. Insertion is not possible.");
    }
    else{
        top++;
        stack[top]=value;
        printf("\nInserted Successfully.");
    }
}
void pop(){
    if(top==-1){
        printf("\nStack is Empty. Deletion not possible.");
    }
    else{
        printf("\nDeleted: %d",stack[top]);
        top--;
    }
}
void display(){
    if(top==-1){
        printf("\nStack is Empty.");
    }
    else{
        int i;
        printf("\nStack elements are:\n");
        for(i=top;i>=0;--i){
            printf("%d\n",stack[i]);
        }
    }
}
void main(){
    int value, choice;
    clrscr();
    while(1){
        printf("\n1.Push\n2.Pop\n3.Display\n4.Exit");
        printf("Enter your choice:");
        scanf("%d",&choice);
        switch(choice){
            case 1:
            printf("Enter the value to be inserted:");
            scanf("%d",&value);
            push(value);
            break;
            case 2:
            pop();
            break;
            case 3:
            display();
            break;
            case 4:
            exit(0);
            default:
            printf("Wrong choice");
        }
    }
}
