# Lab 9 Exercise 4

## Override overridden Method
![alt text](./Pictures/image02.png)
1.สร้าง console application project

```cmd
dotnet new console --name Lab09_Ex04
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
SecondDerivedClass sdRef  = new SecondDerivedClass();
BaseClass bcRef = (BaseClass) sdRef;

sdRef.Print();
bcRef.Print();

class BaseClass
{
    virtual public void Print()
    {
        System.Console.WriteLine("Hello from BaseClass");
    }
}
class DerivedClass : BaseClass
{
    override public void Print()
    {
       System.Console.WriteLine("Hello from DerivedClass");
    }
}
class SecondDerivedClass : DerivedClass
{
    public void Print()
    {
       System.Console.WriteLine("Hello from SecondDerivedClass");
    }
}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab09_Ex04
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3

<img width="686" alt="image" src="https://github.com/chatladawongkanyon/03376836-OOP-2566-Lab-09/assets/144195963/509115be-8f3b-4750-8dac-c08ff92c7593">

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex04
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5

<img width="441" alt="image" src="https://github.com/chatladawongkanyon/03376836-OOP-2566-Lab-09/assets/144195963/3fa8752d-6231-4bc6-a6da-12934dcdf5fd">

7.อธิบายสิ่งที่พบในการทดลอง

โปรแกรมจะแสดงผล
Hello from SecondDerivedClass
Hello from DerivedClass
