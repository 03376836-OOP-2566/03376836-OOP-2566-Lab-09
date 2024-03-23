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
![image](https://github.com/VisawaPRO/03376836-OOP-2566-Lab-09/assets/144195555/ca813460-e9eb-406d-8c76-f1f929fcdaba)
### สามารถ Build ได้ เพราะ ใส่ keyword New เข้าไปทำให้สร้างเมทอดในคลาสลูกจะสร้างเมทอดใหม่ที่ไม่ได้ทับเมทอดในคลาสแม่

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex05
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/VisawaPRO/03376836-OOP-2566-Lab-09/assets/144195555/89311d56-6881-4ba7-8a03-84c37ca7866f)
### สามารถ Run ได้ปกติ
7.อธิบายสิ่งที่พบในการทดลอง
### โปรแแกรมจะแสดงผล
### Hello from SecondDerivedClass
### Hello from DerivedClass
