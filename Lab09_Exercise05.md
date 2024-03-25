# Lab 9 Exercise 5

## Override with `new` keyword
![alt text](./Pictures/image03.png)
1.สร้าง console application project

```cmd
dotnet new console --name Lab09_Ex05
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
    new public void Print()
    {
       System.Console.WriteLine("Hello from SecondDerivedClass");
    }
}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab09_Ex05
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3

<img width="542" alt="image" src="https://github.com/chatladawongkanyon/03376836-OOP-2566-Lab-09/assets/144195963/b7ddc09f-7a5f-4c57-935e-c011c8751194">

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex05
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5

<img width="431" alt="image" src="https://github.com/chatladawongkanyon/03376836-OOP-2566-Lab-09/assets/144195963/7b5f43fd-196e-40c4-b2ee-a3a58c19acde">

7.อธิบายสิ่งที่พบในการทดลอง

Hello from SecondDerivedClass
Hello from DerivedClass
