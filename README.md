Errorr!!!! we can call this() and super() in first line of a constructor but instead we can use them to call a function from one function using . operator

class A
{
	int a;
	A()
	{
		System.out.println("Hello");
	}
	void show()
	{
		this();
	}
}
class B extends A
{
	void show()
	{
		super();
		
	}
}

class Jala 
{
	public static void main(String[] args){
		B b = new B();
			 
	}
}

But can do this

class A
{
	int a;
	A()
	{
		System.out.println("Hello");
	}
	void details()
	{
		System.out.println("Hello there");
	}
	public void show()
	{
		this.details();
	}
}
class B extends A
{
	void print()
	{
		super.show();
	}
}

class Jala 
{
	public static void main(String[] args){
		B b = new B();
		b.print();
	}
}
