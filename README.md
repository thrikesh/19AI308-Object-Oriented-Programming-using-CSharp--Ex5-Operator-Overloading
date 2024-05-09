# 19AI308-Object-Oriented-Programming-using-CSharp--Ex5-Operator-Overloading

## AIM:
To write a C# program to pass values through constructors(default and parameterized) and also overload equal operators by checking whether objects 
are equal using operator overloading. 

## ALGORITHM:
### Step 1:
Initialize a default and a parameterized constructor.

### Step 2:
Overload using equalto symbols.

### Step 3:
Write the code to implement main function.

### Step 4:
Create objects obj1,obj2 and obj3.

### Step 5:
Check the equality.

## PROGRAM:

### DEVELOPED BY : THRIKESWAR
### REGISTER NO : 212222230162

```
using System;
class MyClass
{
    private int value;
    public MyClass()
    {
        this.value = 0;
    }
    public MyClass(int value)
    {
        this.value = value;
    }
    public int GetValue()
    {
        return value;
    }
    public static bool operator ==(MyClass obj1, MyClass obj2)
    {
        if (obj1 is null || obj2 is null)
            return false;
        return obj1.value == obj2.value;
    }
    public static bool operator !=(MyClass obj1, MyClass obj2)
    {
        return !(obj1 == obj2);
    }
}
class Program
{
    static void Main(string[] args)
    {
        MyClass obj1 = new MyClass(10);
        MyClass obj2 = new MyClass(); 
        MyClass obj3 = new MyClass(10);
        Console.WriteLine("Are obj1 and obj2 equal? " + (obj1 == obj2));
        Console.WriteLine("Are obj1 and obj3 equal? " + (obj1 == obj3));
    }
}
```
## OUTPUT:
![image](https://github.com/22008686/19AI308-Object-Oriented-Programming-using-CSharp--Ex5-Operator-Overloading/assets/118916413/8be35424-35be-41c7-bc95-a8da2ad8522a)

## RESULT:
Thus,the program to illustrate operating overloading is successfully implemented.
