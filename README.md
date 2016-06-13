# Liftor
# This program stops the lift on alternate floors
#the following code is executed on BlueJ
import java.io.*;
class liftor
{
public static void main(String[ ] args) throws IOException
{
BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
int date;
System.out.println("Enter Date");
date=Integer.parseInt(br.readLine());
int n=15; //we have assumed the number of floors as 15
int[] floor;
floor=new int[15];
int s=0, i, j, temp, x=0;
System.out.println("Enter Floor Numbers");
for(i=s;floor[i]<=n;i++)
{
floor[i]=Integer.parseInt(br.readLine());
if (floor[i]>n)
break;
s++;
}
for(i=0;i<s;i++)
{
        for(j=0;j<s;j++)
            {
                    if(floor[j]>floor[j+1])
                        {
                            temp=floor[j];
                            floor[j]=floor[j+1];
                            floor[j+1]=temp;
                        }
                }
}
System.out.println("Entered Floor Numbers are:");
for(i=0;i<s;i++)
System.out.println(floor[i]);
System.out.println("Stopping Floors Are:");
if(date%2==0)
{
    for(i=0;i<s;i++)
    {
        if(floor[i]%2==0)
System.out.println(floor[i]);
        else 
System.out.println(floor[i]-1);
  
    }
}
else
{
    for(i=0;i<s;i++)
    {
        if(floor[i]%2==1)
        System.out.println(floor[i]);
        else 
       System.out.println(floor[i]-1);
     
    }
}
}
}


