import java.io.*;
import java.lang.*;
import java.util.*;
class Node
{
    int data;
    Node left,right;
    Node(int data)
    {
        this.data=data;
    }
}

public class Main
{
    static Node Insert(Node root,int x)
{
    if(root==null)
    {
        root = new Node(x);
        return  root;
    }
    if(x<root.data)
    {
        root.left = Insert(root.left,x);
    }
    else if(x>root.data)
    {
        root.right = Insert(root.right,x);
    }
    return root;
}
static void Inorder(Node root)
{
    if(root==null)
       return;
    Inorder(root.left);
    System.out.println(root.data + " ");
    Inorder(root.right);
}

	public static void main(String[] args) {
	    Node root=null;
	    int x;
	    while(true)
	    {
	        Scanner sc = new Scanner(System.in);
	        System.out.println("Enter x:");
	        x=sc.nextInt();
	        if(x==0)
	          break;
	        root=Insert(root,x);
	    }
	    Inorder(root);
		
	}
}
