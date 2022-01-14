# dsa_1_array
Array Operations


#include<stdio.h>
#include<stdlib.h> 

int arr[10],n,i,choice,pos,x,d;

void create()
{
    printf("enter the size of array\n");
    scanf("%d",&n);
    for (i = 0; i < n; i++)
    {
        printf("enter the no %d element of the array\n", i);
        scanf("%d", &arr[i]); 
    }
}

void display()
{
    for (i = 0; i < n; i++)
    {
        printf("\nthe no %d element of the array is %d",i,arr[i]);
    }
}

void insert()
{
    printf("enter the position you want to insert the element");
    scanf("%d",&pos);
    printf("enter the element you want to insert");
    scanf("%d",&x);
    for(i=n-1;i>=pos;i--)
    {
        arr[i+1]=arr[i];

    }
    arr[pos]=x;
    n=n+1;
}

void delete()
{
    printf("enter the postion of element you want to delete :");
    scanf("%d",&d);
    for(i=d;i<n-1;i++)
    {
        arr[i]=arr[i+1];
        n=n-1;
    }
}

void main()
{
    do{
        printf("\n_______________________________________\n");
        printf("\n create 1 \n display 2 \n exit 3 \n insert 4 \n delete 5 \n");
        scanf("%d", &choice);
        printf("\n_______________________________________\n");
        switch(choice)
        {
            case 1: create();
            break;  

            case 2: display();
            break;

            case 3: exit(0);
            break;

            case 4: insert();
            break;

            case 5: delete();
            break;

            default: printf("\ninvalid statement");
            break;
        }
    } while(choice!=3);

}
