import java.io.*;
import java.util.*;
import java.lang.*;
 class Node
{
    int data;
    Node left,right;
    Node(int data)
    {
        this.data=data;
        left=null;
        right=null;
    }
}
public class Main
{
    static Node Insert(Node root,int x)
    {
        if(root==null)
        {
            root = new Node(x);
            return root;
        }
        Queue<Node> q = new LinkedList<Node>();
        q.add(root);
        while(!q.isEmpty())
        {
            Node temp=q.peek();
            q.remove();
            if(temp.left==null)
            {
                temp.left= new Node(x);
                return root;
            }
            else
             q.add(temp.left);
            if(temp.right==null)
            {
                temp.right= new Node(x);
                return root;
            }
            else
              q.add(temp.right);
        }
        return root;
        
    }
    static void Inorder(Node root)
    {
        if(root==null)
          return;
        Inorder(root.left);
        System.out.print(root.data+" ");
        Inorder(root.right);
    }
	public static void main(String[] args) {
		Node root=null;
		int x;
		while(true)
		{
		    Scanner sc=new Scanner(System.in);
		    System.out.println("Enter x:");
		    x=sc.nextInt();
		    if(x==0)
		       break;
		    root=Insert(root,x);
		}
		System.out.print("Inorder:");
		Inorder(root);
	}
}

-------------------------------------------------------------------------------------------------------------------------------


include <iostream>
#include <bits/stdc++.h>
using namespace std;

struct node
{
    int data;
    struct node* left;
    struct node* right;
};
struct node *getNode(int x)
{
    struct node *t = (struct node*)malloc(sizeof(struct node));
    t->data=x;
    t->left=NULL;
    t->right=NULL;
    return t;

}
struct node *Insert(struct node* root,int data)
{
    if(root == NULL)
    {
        root= getNode(data);
        return root;
    }
    queue<node*> q;
    q.push(root);
    while(!q.empty())
    {
        node* temp = q.front();
        q.pop();
        if(temp->left != NULL)
        {
            q.push(temp->left);
        }
        else
        {
            temp->left = getNode(data);
            return root;
        }
        if(temp->right != NULL)
        {
            q.push(temp->right);
        }
        else
        {
            temp->right = getNode(data);
            return root;
        }
    }
    return root;
}

void Inorder(struct node *root)
{
    if(root==NULL)
        return;
    Inorder(root->left);
    printf("%d ",root->data);
    Inorder(root->right);
}
int main()
{
    struct node *root;
    while(1)
    {
        int x;cout<<"enter x:";cin>>x;
        if(x==0)
            break;
        root=Insert(root,x);
    }
    Inorder(root);
}


