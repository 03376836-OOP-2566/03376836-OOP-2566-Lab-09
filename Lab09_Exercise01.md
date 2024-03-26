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
![image](https://github.com/65030121natthamon/03376836-OOP-2566-Lab-09/assets/144195611/ac3e74b0-d8fe-4fa4-aedc-8305889d1766)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex01
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/65030121natthamon/03376836-OOP-2566-Lab-09/assets/144195611/bb2c6be1-eca1-4fe8-b98c-bcca0e134372)

7.อธิบายสิ่งที่พบในการทดลอง
- เป็นการเรียกใช้เมทอด Info() ในแต่ละคลาส เมทอดที่ถูกเรียกใช้จะขึ้นต้นด้วยข้อความที่ถูกกำหนดในคลาส
- คลาสBaseClassจะประกาศเมทอด เป็นvirtual และสามารถถูกoverride ได้ในคลาสลูก 
