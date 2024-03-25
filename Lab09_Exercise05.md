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

![5](https://github.com/Siriratda/03376836-OOP-2566-Lab-09/assets/144195995/a05a2c4b-fa7b-481e-abef-9cb31ada4270)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex05
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5

![5 1](https://github.com/Siriratda/03376836-OOP-2566-Lab-09/assets/144195995/214db591-67ed-41d2-a090-35e36ba6f0a1)

7.อธิบายสิ่งที่พบในการทดลอง

สามารถ Run ได้ปกติ
โปรแแกรมจะแสดงผล
Hello from SecondDerivedClass
Hello from DerivedClass
