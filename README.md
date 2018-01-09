# 网易云课堂：丝竹悦耳

n-m个素数之和,0<n<=m<200.

可以被1和本身整除的数为素数,1不是素数.

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner in = new Scanner(System.in);
		int n = in.nextInt();
		int m = in.nextInt();
		int sum = 0;
		int cnt = 1;
		int a = 2;
		if(n>0 && n<=m && m<=200)
		{
		for( int i = 2; i<=a; i++)
		{
			boolean isprime = true;
			for( int k =2; k<i; k++)
			{
				if( i%k==0)
				{
					isprime = false;
					break;
				}
			}
			if( isprime == true)
			{
				if(cnt>=n && cnt<=m)
				{
				sum = sum +i;
				}
				if(cnt==m)
				{
					break;
				}
				cnt++;
			}
			a++;
		}
			System.out.println(sum);
		}
	}
}
