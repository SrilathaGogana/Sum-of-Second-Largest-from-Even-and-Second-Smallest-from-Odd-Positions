# Sum-of-Second-Largest-from-Even-and-Second-Smallest-from-Odd-Positions
The function accepts an integers arr of size 'length' as its arguments you are required to return the sum of second largest element from the even positions and second smallest from the odd position of given 'arr'
package javaproject;
import java.util.*;
//import java.util.ArrayList;
//import java.util.Collections;
public class ArrayPractice5{
	public int  SumOfEvenPosiEleAndOddPosiEle(int arr1[]) {
		if(arr1.length<=3 || arr1.length==0 )
			return 0;
		ArrayList even=new ArrayList();
		ArrayList odd=new ArrayList();
		for(int i=0;i<arr1.length;i++) {
			if(i%2==0)
				 even.add(arr1[i]);
			else
				 odd.add(arr1[i]);
		}
		Collections.sort(even);
		Collections.sort(odd);
	return (int) even.get(even.size()-2)+(int) odd.get(1);
	}
	public static void main(String args[]) {
		Scanner sc=new Scanner(System.in);
		int n=sc.nextInt();
		int arr1[]=new int[n];
		for(int i=0;i<n;i++)
		  arr1[i]=sc.nextInt();
		ArrayPractice5 obj=new ArrayPractice5();
		System.out.println(obj.SumOfEvenPosiEleAndOddPosiEle(arr1));
	}
}
