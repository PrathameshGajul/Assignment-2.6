Q1.Write a program to accepts two numbers from stdin and find all the odd as well as even
numbers present in between them.
Ans:
import java.util.Scanner; 
import java.util.ArrayList;
import java.util.Collections;

public class Main {

public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int x=sc.nextInt();   //Accept first number
    int y=sc.nextInt();   //Accept second number
    ArrayList<Integer> e = new ArrayList<Integer>();    //ArrayList to store the even numbers
    ArrayList<Integer> o = new ArrayList<Integer>();     //ArrayList to store the odd numbers
    for(int i=x;i<=y;i++)    //Iterating in the given range
    {
        if(i%2==0)    //condition for satisfying even number
        {
            e.add(i);
        }
        else
        {
            o.add(i);
        }
    }
    System.out.println("Even Numbers are:");
    Collections.sort(e);            //sort even numbers
    System.out.println(e);          //display even numbers
    System.out.println("Odd Numbers are:");
    Collections.sort(o);            //sort odd numbers
    System.out.println(o);          //display odd numbers
    sc.close();
}


Q2.Joe is scared to go to school. When her dad asked the reason, joe said she is unable to
complete the task given by her teacher. The task was to find the “first 10 multiples” of the
number entered from stdin.
Ans:
import java.util.Scanner;
import java.util.ArrayList;
import java.util.Collections;

public class Main {

public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int x=sc.nextInt();     // Input the number for getting 10 multiples of that number

    int a[] = new int[10];  //to store result

    for(int i=0;i<10;i++)    //Iterating in the given range
    {
        a[i] = x*(i+1);
    }
    System.out.println("Multiple of the entered numbers:");
    for(int j=0;j<10;j++)  // to display the first 10 multiples of the number
    {
        System.out.println(a[j]);
    }
        sc.close();
}
}


Q3.Write a program consisting method sum() and demonstrate the concept of method
overloading using this method.
Ans:

import java.util.*;
public class Main {

public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    int x=sc.nextInt();//Input number
    int y=sc.nextInt();//Input number
    int z =sc.nextInt(); //Input number
    sum(x,y);   //sum method called with two variables
    sum(x,y,z); //sum method called with three variables
    sc.close();
}
static void sum(int x,int y)   //method to add two numbers
{
    int a;
    a=x+y;
    System.out.println("Method with two variables");
    System.out.println(a);   //print obtained result
}
static void sum(int x,int y,int z)   //method to multiply two number and add third number
{
    int a;
    a=x*y+z;
    System.out.println("Method with two variables"+"\n"+a);   //print obtained result
}
