# pay-off

pay off

Problem Description

作为清华的学生，最盼望的日子就是发工资的日子，养家糊口就靠它了，呵呵
但是对于学校财务处的工作人员来说，这一天则是很忙碌的一天，财务处的小胡老师最近就在考虑一个问题：如果每个老师的工资额都知道，最少需要准备多少张人民币，才能在给每位老师发工资的时候都不用老师找零呢？
这里假设老师的工资都是正整数，单位元，人民币一共有100元、50元、10元、5元、2元和1元六种。 


Input

输入数据包含多个测试实例，每个测试实例的第一行是一个整数n（n<100），表示老师的人数，然后是n个老师的工资。

n=0表示输入的结束，不做处理。 


Output

对于每个测试实例输出一个整数x,表示至少需要准备的人民币张数。每个输出占一行。

 
Sample Input

3

1 2 3

0 


Sample Output

4 

 
解答：

#include<stdio.h>

main()

{

    int n,m,a,b,c,d,e,f,i,j,k;
    
    while(scanf("%d",&n)!=EOF&&n!=0)
    
    {
    
        k=0;
        
        for(i=0;i<n;i++)
        
        {
        
            scanf("%d",&m);
            
             a=m/100;
             
             b=m%100/50;
             
             c=m%100%50/10;
             
             d=m%100%50%10/5;
             
             e=m%100%50%10%5/2;
             
             f=m%100%50%10%5%2;
             
             k=k+a+b+c+d+e+f;
             
        }
        
        printf("%d\n",k);
        
    }
    
}

