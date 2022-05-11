# linklist
#include<iostream.h>
#include<conio.h>
class linklist
{
int ele,data;
linklist *start,*link,*move,*next;
public:
linklist()
{
start=NULL;
}
void insertbeg();
void search();
void show();
void count();
};
void linklist::insertbeg()
{
cout<<"enter elements"<<endl;
cin>>ele;
linklist *node;
node=new linklist();
node->data=ele;
node->link=NULL;
if(start==NULL)
{
start=node;
}
else
{
node->link=start;
start=node;
}
}
void linklist::show()
{
if(start==NULL)
{
cout<<"node is empty"<<endl;
}
else
{
move=start;
while(move!=NULL)
{
cout<<move->data;
move=move->link;
}
}
}
void linklist::search()
{
int s;
cout<<"enter element to search"<<endl;
cin>>s;
if(start==NULL)
{
cout<<"node is empty"<<endl;
}
else
{
move=start;
while(move!=NULL)
{
if(move->data==s)
{
cout<<"data found"<<endl;
move=move->next;
}
else
{
cout<<"data not found"<<endl;
move=move->next;
}
}
}
}

void main()
{
clrscr();
linklist l;
int ch;
cout<<"1.insertbeg,2.show,3.search,4.exit"<<endl;
while(ch!=6)
{
cout<<"enter your choise"<<endl;
cin>>ch;
switch(ch)
{
case 1:l.insertbeg();break;
case 2:l.show();break;
case 3:l.search();break;
case 4:exit(0);
default:cout<<"you entered wrong choise"<<endl;
}
}
getch();
}
