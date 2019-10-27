# data-lab
DATA LAB code(Delete item in array using by c)
#include<stdio.h>
#define success_value 99999
#define null_value -99999
int list[5];
int length;
void initialize()
{
    length=0;
}
void insertItem(int value)
{
    list[length]=value;
    length=length+1;
    //return success_value;
}
void print()
{
    int i;
    for(i=0;i<length;i++)
    {
        printf("%d ",list[i]);
    }
}
int getItem(int pos)
{
int res;
res=list[pos];
return res;
}
int deleteItemAt(pos)
{
    if(pos>=0 && pos<length)
    {
    list[pos] = list[length-1];
    length = length -1;
    return success_value;
    }
    else
    {
        return null_value;
    }
}
int main()
{
    int c,input,ret;
    initialize();
    //scanf("%d",&input);
    insertItem(10);
    //scanf("%d",&input);
    insertItem(20);
    //scanf("%d",30);
    insertItem(30);
    insertItem(40);
    insertItem(50);
    //c=getItem(2);
    print();
    printf("\n");
    //printf("%d",c);
    ret = deleteItemAt(5);
    if(ret == success_value)
    {
        printf("successfully deleted\n");
    }
        else
        {
            printf("not deleted\n");
        }
        print();
}
