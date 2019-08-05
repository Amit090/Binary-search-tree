# Binary-search-tree
/******************************************************************************

                            Online Java Compiler.
                Code, Compile, Run and Debug java program online.
Write your code in this editor and press "Run" button to execute it.

*******************************************************************************/




import java.util.Scanner;
public class Main
{
	public static void main(String[] args) {
		System.out.println("Hello World");
		
		int location=-1;
		Scanner sc = new Scanner(System.in);
	    int n = sc.nextInt();
	    int arr[] = new int [100];
	    for(int i=0;i<n;i++)
	        arr[i] = sc.nextInt();
	    int item = sc.nextInt();
	    
	    location = BST(arr,0,9,item);
	    System.out.println("LOCATION = "+location);
}
public static int BST(int arr[],int beg,int end,int item)
{
    int mid;
    if(end>=beg)
    {
        mid=(beg+end)/2;
        if(arr[mid]==item)
            return mid+1;
            
        else if(arr[mid]>item)
            return BST(arr,beg,mid-1,item);
            
        else 
            return BST(arr,mid+1,end,item);
    }        
        
            return -1;
    
}
	}

