# array-reversal
reversing array with inplace algorithm
//INPLACE ALGORITHM:
// Iterate the loop from zeroth index to middle index
// First iteration:swap the first index with last index 
// next iteration: Increase the index to first+1 and swap it with index last-1 and continue until reaching the middle index

// PROGRAM CODE:
import java.util.*;
public class Main
{
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int i, temp;
		System.out.println("ENTER THE NO.OF ELEMENTS IN THE ARRAY: ");
		int n = sc.nextInt();
		int arr[] = new int[n];
		System.out.println("ENTER THE ELEMENTS: ");
		
		// inserting elements into an array
		for(i = 0; i < n; i++)
		{
		    arr[i] = sc.nextInt();
		}
		
		//inplace algorithm with O(N) complexity
		for(i = 0; i < n / 2; i++)
		{
		    temp = arr[i];
		    arr[i] = arr[n - i - 1];
		    arr[n - i - 1] = temp;
		}
		System.out.println("THE REVERSED ARRAY IS: ");
		  
		//printing reversed array
     for(i = 0; i < n; i++)
     {
         System.out.println(arr[i]);
     }
	}
}
  
