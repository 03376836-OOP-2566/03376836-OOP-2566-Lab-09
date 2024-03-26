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
![image](https://github.com/ThanchiraCharakhon099/03376836-OOP-2566-Lab-09/assets/144195708/df15d25b-b993-47e2-9560-38603d4a2936)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex01
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/ThanchiraCharakhon099/03376836-OOP-2566-Lab-09/assets/144195708/c2600a64-9677-4397-9ae5-bebf6c95ee18)

7.อธิบายสิ่งที่พบในการทดลอง
สร้างอ็อบเจกต์ dcRef จากคลาส DerivedClass ด้วย DerivedClass dcRef = new DerivedClass(); 
และสร้างอ็อบเจกต์ bcRef จากคลาส BaseClass ด้วย BaseClass bcRef = new BaseClass(); 
และเรียกใช้เมทอด Info() ของทั้ง dcRef และ bcRef

ผลลัพธ์ที่ได้
This is DerivedClass
This is BaseClass

