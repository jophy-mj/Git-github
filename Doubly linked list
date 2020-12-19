#include<stdio.h>
#include<conio.h>
#include<process.h>
#include<stdlib.h>
struct node
{
int data;
struct node *prev;
struct node *next;
}*start=0,*temp,*ptr;
void creation();
void insertbeg();
void insertend();
void insertpos();
void deletionbeg();
void deletionend();
void deletionpos();
void traversal();
void search();
void main()
{
int s;
clrscr();
while(1)
{
printf("\n\n1.CREATION\n2.INSERTION AT BEGINING\n3.INSERTION AT END\n4.INSERTION IN BETWEEN\n5.DELETION AT BEGINING\n6.DELETION AT END\n7.DELETION IN BETWEEN\n8.TRAVERSAL\n9.SEARCH\n10.EXIT\n\n");
printf("Enter the choice:");
scanf("%d",&s);
switch(s)
{
case 1:creation();
       break;
case 2:insertbeg();
	break;
case 3:insertend();
       break;
case 4:insertpos();
       break;
case 5:deletionbeg();
       break;
case 6:deletionend();
       break;
case 7:deletionpos();
       break;
case 8:traversal();
       break;
case 9:search();
       break;
case 10:exit(0);
       break;
default:printf("Invalid Choice!");
	break;
}
}
}
void creation()
{
int item;
printf("Enter the item:\n");
scanf("%D",&item);
ptr=(struct node *)malloc(sizeof(struct node));
ptr->data=item;
ptr->next=0;
if(start==0)
{
start=ptr;
ptr->prev=0;
}
else
{
temp=start;
while(temp->next!=0)
{
temp=temp->next;
}
temp->next=ptr;
ptr->prev=temp;
}
}
void insertbeg()
{
int item;
printf("Enter the item:\n");
scanf("%d",&item);
ptr=(struct node *)malloc(sizeof(struct node));
ptr->data=item;
ptr->prev=0;
ptr->next=start;
start->prev=ptr;
start=ptr;
}
void insertend()
{
int item;
printf("Enter the item:\n");
scanf("%d",&item);
ptr=(struct node *)malloc(sizeof(struct node));
ptr->data=item;
temp=start;
while(temp->next!=0)
{
temp=temp->next;
}
temp->next=ptr;
ptr->prev=temp;
ptr->next=0;
}
void insertpos()
{
int item,pos,i,f=0;
printf("Enter the position:\n");
scanf("%d",&pos);
if(pos==1)
{
insertbeg();
}
else
{
temp=start;
for(i=1;i<pos-1;i++)
{
temp=temp->next;
if(temp==0)
{
printf("Invalid Position\n");
f=1;
break;
}
}
if(f==0)
{
printf("Enter the item:\n");
scanf("%d",&item);
ptr=(struct node *)malloc(sizeof(struct node));
ptr->data=item;
ptr->next=temp->next;
temp->next=ptr;
ptr->prev=temp;
}
}
}
void deletionbeg()
{
if(start==0)
{
printf("Empty\n\n");
}
else
{
temp=start;
start=start->next;
start->prev=0;
printf("%d is Deleted\n",temp->data);
free(temp);
}
}
void deletionend()
{
if(start==0)
{
printf("Empty\n\n");
}
else
{
ptr=start;
while(ptr->next->next!=0)
{
ptr=ptr->next;
}
temp=ptr->next;
ptr->next=0;
printf("%d is Deleted\n",temp->data);
free(temp);
}
}
void deletionpos()
{
int pos,i,f=0;
if(start==0)
{
printf("Empty\n\n");
}
else
{
printf("Enter the position to be deleted:\n");
scanf("%d",&pos);
if(pos==1)
{
deletionbeg();
}
else
{
ptr=start;
for(i=1;i<pos-1;i++)
{
ptr=ptr->next;
if(ptr==0)
{
printf("Invalid Position\n");
f=1;
break;
}
}
if(f==0)
{
temp=ptr->next;
ptr->next=temp->next;
temp->next->prev=ptr;
printf("%d is deleted\n\n",temp->data);
free(temp);
}
}
}
}
void traversal()
{
if(start==0)
{
printf("Empty\n\n");
}
else
{
temp=start;
while(temp!=0)
{
printf("%d\t",temp->data);
temp=temp->next;
}
}
}
void search()
{
int item,f=0;
printf("Enter the item to be searched:\n");
scanf("%d",&item);
temp=start;
while(temp!=0)
{
if(temp->data==item)
{
f=1;
break;
}
temp=temp->next;
}
if(f==1)
{
printf("ITEM IS FOUND\n\n");
}
else
{
printf("ITEM IS NOT FOUND");
}
}
