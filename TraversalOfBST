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
    System.out.print(root.data + " ");
    Inorder(root.right);
  }
   static void Preorder(Node root)
 {
    if(root==null)
       return;
    System.out.print(root.data + " ");
    Preorder(root.left);
    
    Preorder(root.right);
  }
   static void Postorder(Node root)
 {
    if(root==null)
       return;
    Postorder(root.left);
    
    Postorder(root.right);
    System.out.print(root.data + " ");
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
	    System.out.print("Inorder");
	    Inorder(root);
	     System.out.print("Preorder");
	    Preorder(root);
	     System.out.print("Postorder");
	    Postorder(root);
		
	}
}
