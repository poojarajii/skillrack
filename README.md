import java.util.Scanner;
public class Interlacedstring {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        String str=sc.next();
        int n=sc.nextInt();
        String str1="";
        String str2="";
        int x,y,z;
        
        char c[]=str.toCharArray();
        int m=0;
        m=c.length-n;
        if(n<m)
        {
            x=0;
            y=1;
            z=n;
        }
        else
        {
            x=1;
            y=0;
            z=m;
        }
        for(int i=x;i<c.length && i<(z*2);i+=2)
        {
            str1=str1+c[i];
        }
        for(int i=y;i<c.length;)
        {
            if(i<(z*2)-1)
            {
                str2=str2+c[i];  
                i+=2;
            }
            else
            {
                str2=str2+c[i];
                i++;
            }
        }
        if(x==0)
        {
        System.out.println(str1);
        System.out.println(str2);
        }
        else
        {
        System.out.println(str2);
        System.out.println(str1);
        }
 }
}
