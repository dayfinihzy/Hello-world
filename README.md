# Hello-world
#include <stdio.h>
int main()
{
    int n,i,k;
    char s[100];
    printf("请输入向前推几位字母：\n");
    scanf("%d",&n);
    printf("请输入小写字母，输入其他（除空格外）结束读入\n");
    
    for(i=0;i<100;i++)
    {
         scanf("%c",&s[i]);
        if((s[i]<'a'||s[i]>'z')&&(s[i]!=' '))
            break;
    }
    k=i;
    for(i=0;i<=k;i++)
    {
        if(s[i]>='a'&&s[i]<=122-n)
            s[i]=s[i]+n;
         else if(s[i]>=123-n&&s[i]<='z')
             s[i]=s[i]-(26-n);
        printf("%c",s[i]);
    }
    return 0;
}
