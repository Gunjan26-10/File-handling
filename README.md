# File-handling
Developed by gunjan narkhede
#include<stdio.h>
#include<string.h>
int main()
{
	FILE *ptr1,*ptr2,*ptr3;
	char str[1000];
	int i=0,len,k;
	ptr1=fopen("temp.txt","r");
	ptr2=fopen("temp1.txt","w");
	printf("files are reading");
	str[i]=getc(ptr1);
	while(str[i]!=EOF)
	{
		i++;
		str[i]=getc(ptr1);
	}
	for(k=i;k<=0;k--)
	{
		fprintf(ptr2,"%c",str[k]);
	}
	fclose(ptr2);
	ptr3=fopen("temp2.txt","w");
        for(k=0;k<=i;k++)
        {
                fprintf(ptr3,"%c",str[k]);
        }
        printf("done");
        fclose(ptr1);
        fclose(ptr3);
        return 0;
}
