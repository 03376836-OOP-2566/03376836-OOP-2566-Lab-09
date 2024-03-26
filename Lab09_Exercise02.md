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
![image](https://github.com/ThanchiraCharakhon099/03376836-OOP-2566-Lab-09/assets/144195708/9da21c19-4ad6-429b-a3b0-c84bc44c7c78)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex02
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/ThanchiraCharakhon099/03376836-OOP-2566-Lab-09/assets/144195708/c579169c-02e8-4bc3-82f4-aede4a7b74f5)

7.อธิบายสิ่งที่พบในการทดลอง
เมื่อทำการสร้าง DerivedClass ด้วย DerivedClass dcRef = new DerivedClass(); และทำการ cast dcRef เป็น BaseClass ด้วย (BaseClass) dcRef จะได้ bcRef ซึ่งเป็นอ็อบเจกต์ของ BaseClass ที่อ้างอิงไปยัง DerivedClass ซึ่งมีผลทำให้เมื่อเรียกใช้งานเมธอด Info() ของทั้ง dcRef และ bcRef 

ผลลัพธ์
This is DerivedClass
This is DerivedClass
