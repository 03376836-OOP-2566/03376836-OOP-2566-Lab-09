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

![2](https://github.com/Siriratda/03376836-OOP-2566-Lab-09/assets/144195995/a13030c6-0235-49d0-9320-3504b3e7caab)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex02
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5

![2 1](https://github.com/Siriratda/03376836-OOP-2566-Lab-09/assets/144195995/6c923e77-1efc-4292-9884-8c87ac02d36e)

7.อธิบายสิ่งที่พบในการทดลอง

สามารถ Run ได้ เพราะ dcRef.Info() จะเรียกใช้เมทอด Info() จากคลาสที่สืบทอด (DerivedClass) และ bcRef.Info() จะเรียกใช้เมทอด Info() จากคลาสฐาน (BaseClass)
โปรแกรมจะแสดงผล
This is DerivedClass
This is DerivedClass
