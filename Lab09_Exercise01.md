# Lab 9 Exercise 1

## Polymorphism (virtual-override methods)

1.สร้าง console application project

```cmd
dotnet new console --name Lab09_Ex01
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
DerivedClass dcRef = new DerivedClass();
BaseClass bcRef = new BaseClass();

dcRef.Info();
bcRef.Info();

class BaseClass
{
    virtual public void Info()
    {
        System.Console.WriteLine("This is BaseClass");
    }
}

class DerivedClass : BaseClass
{
    override public void Info()
    {
        System.Console.WriteLine("This is DerivedClass");
    }
}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab09_Ex01
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3

<img width="545" alt="image" src="https://github.com/chatladawongkanyon/03376836-OOP-2566-Lab-09/assets/144195963/72cebac7-92a5-465d-b601-aafc45a7429f">

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex01
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5

<img width="408" alt="image" src="https://github.com/chatladawongkanyon/03376836-OOP-2566-Lab-09/assets/144195963/54c344e4-9a98-4be2-904a-4c83673b59da">

7.อธิบายสิ่งที่พบในการทดลอง
โปรแกรมจะแสดงผล
This is DerivedClass
This is BaseClass
