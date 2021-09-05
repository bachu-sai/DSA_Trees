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
  static int Height(Node root)
  {
      if(root==null)
        return 0;
      return 1+Math.max(Height(root.left),Height(root.right));
      
  }
  static void ZigZag(Node root)
  {
      Stack<Node> s1= new Stack<Node>();
      Stack<Node> s2= new Stack<Node>();
      s1.push(root);
      while(s1.empty()||s2.empty())
      {
      while(!s1.empty())
      {
          Node  t=s1.peek();
          s1.pop();
          System.out.println(t.data+" ");
          if(t.left!=null)
          {
              s2.push(t.left);
              
          }
          if(t.right!=null)
          {
            s2.push(t.right);
          } 
          
      }
      while(!s2.empty())
      {
          Node t1=s2.peek();
          s2.pop();
          System.out.println(t1.data+" ");
          if(t1.right!=null)
          {
              s1.push(t1.right);
              
          }
          if(t1.left!=null)
          {
            s1.push(t1.left);
          } 
      }
      }
      
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
	    System.out.print("Height :"+Height(root));
	     System.out.print("ZigZag :");
	    ZigZag(root);
	    
		
	}
}
