# Lab 9 Exercise 2

## virtual-override methods

1.สร้าง console application project

```cmd
dotnet new console --name Lab09_Ex02
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
DerivedClass dcRef = new DerivedClass();
BaseClass bcRef =  (BaseClass) dcRef;

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
dotnet build  Lab09_Ex02
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3

<img width="532" alt="image" src="https://github.com/chatladawongkanyon/03376836-OOP-2566-Lab-09/assets/144195963/6d6d1a8c-a71a-45ef-b87f-792d66628747">

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex02
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5

<img width="419" alt="image" src="https://github.com/chatladawongkanyon/03376836-OOP-2566-Lab-09/assets/144195963/9d0e723c-9f4c-4c5d-9f24-c18bc8a7a30d">

7.อธิบายสิ่งที่พบในการทดลอง

โปรแกรมจะแสดงผล
This is DerivedClass
This is DerivedClass
