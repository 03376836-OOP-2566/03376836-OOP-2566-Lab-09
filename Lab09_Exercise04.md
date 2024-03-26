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
![image](https://github.com/65030121natthamon/03376836-OOP-2566-Lab-09/assets/144195611/5f1ace95-2dac-4a38-a600-1dd698a66dd1)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex04
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/65030121natthamon/03376836-OOP-2566-Lab-09/assets/144195611/59d51c7d-698e-4007-b0e9-b07344936e06)

7.อธิบายสิ่งที่พบในการทดลอง
- BaseClass มีเมทอด Print() ที่ถูกประกาศเป็น virtual เมทอดนี้สามารถถูก override ได้ในคลาสลูก

- DerivedClass เราทำการ override เมทอด Print() ที่ถูกสืบทอดมาจาก BaseClass และให้มันพิมพ์ข้อความ "Hello from DerivedClass"

- SecondDerivedClass เราไม่ได้ใช้คำสำคัญ override แต่เป็นการให้เมทอดใหม่ในคลาสลูก จะเป็นแบบ shadowing ทำให้ไม่สามารถเรียกใช้เมทอด Print() ของคลาสแม่ผ่านอ็อบเจกต์ของคลาสลูกได้

- sdRef.Print() เป็นการเรียกใช้เมทอด Print() ของ SecondDerivedClass ซึ่งจะพิมพ์ "Hello from SecondDerivedClass" ออก
