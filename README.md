# vardh7112002-Single-level-Inheritance-Ex1

import java.util.Scanner;
class A{
    private int x;
   
    A(){
        x=1;
    }
    
    A(int x)
    {
        this.x=x;
    }
   
    void setdata(int x)
    {
        this.x=x;
    }
   
    void getdata()
    {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter value of x: ");
        x=sc.nextInt();
    }
    void display()
    {
        System.out.println(x);
    }
}
class B extends A {
    private int y;
    B()
    {
        super();    // optional
        y=0;
    }
    
    B(int x,int y)
    {
        super(x);    //Compulsory
        this.y=y;
    }
    void setdata(int x, int y)
    {
        this.y=y;
        setdata(x);
    }
    
    void getdata()
    {
        Scanner sc= new Scanner(System.in);
        System.out.print("Enter value of y: ");
        y=sc.nextInt();
    }
    void display()
    {
        super.display();
        System.out.println(y);
    }
    
}

public class ABTest {
    
    public static void main(String args[]) {
    
    B b1=new B();
    b1.setdata(5,10);
    b1.display();
        
    }
}
