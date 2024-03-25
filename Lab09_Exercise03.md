# Lab 9 Exercise 3

## Override overridden Method
![alt text](./Pictures/image01.png)

1.สร้าง console application project

```cmd
dotnet new console --name Lab09_Ex03
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
    override public void Print()
    {
       System.Console.WriteLine("Hello from SecondDerivedClass");
    }
}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab09_Ex03
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3

![3](https://github.com/Siriratda/03376836-OOP-2566-Lab-09/assets/144195995/d1271a0a-bb27-4f83-99d0-8b002ef635da)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex03
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5

![3 1](https://github.com/Siriratda/03376836-OOP-2566-Lab-09/assets/144195995/b3f28f55-b447-4769-a8c3-7958e25d8e27)

7.อธิบายสิ่งที่พบในการทดลอง

สามารถ Run ได้ เพราะ เรียกเมทอด Print() เรียกบนอ็อบเจกต์ของคลาส SecondDerivedClass ซึ่่ง ผลลัพธ์จากเมทอดที่ถูกโอเวอร์ไรด์ในคลาส SecondDerivedClass
โปรแกรมจะแสดงผล
Hello from SecondDerivedClass
Hello from SecondDerivedClass
