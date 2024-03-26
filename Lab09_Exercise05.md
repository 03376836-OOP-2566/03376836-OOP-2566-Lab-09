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
![image](https://github.com/65030121natthamon/03376836-OOP-2566-Lab-09/assets/144195611/84d93ddb-b3a0-45a5-aaf9-00d31068c0ea)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex05
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/65030121natthamon/03376836-OOP-2566-Lab-09/assets/144195611/40a6ca27-60a9-462c-96fe-7a8cbcb72b97)

7.อธิบายสิ่งที่พบในการทดลอง
- sdRef.Print() จะเป็นการเรียกใช้เมทอด Print() ของ SecondDerivedClass ซึ่งจะพิมพ์ "Hello from SecondDerivedClass" ออกทางหน้าจอ
- BaseClass จะไม่สามารถเรียกใช้เมทอดใหม่ที่ถูกประกาศใน SecondDerivedClass ได้ เรียกใช้ bcRef.Print() จะเป็นการเรียกใช้เมทอด Print() ของ BaseClass ซึ่งจะพิมพ์ "Hello from BaseClass" ออกทางหน้าจอ
