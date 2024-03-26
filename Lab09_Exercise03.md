ฆ# Lab 9 Exercise 3

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
![image](https://github.com/65030121natthamon/03376836-OOP-2566-Lab-09/assets/144195611/07b757fa-5d78-4804-9786-1ce78254742b)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex03
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/65030121natthamon/03376836-OOP-2566-Lab-09/assets/144195611/2114d76a-fac3-4b1c-a90b-43b0c18b842d)

7.อธิบายสิ่งที่พบในการทดลอง
- BaseClass เรามีเมทอด Print() ที่ถูกประกาศเป็น virtual เมทอดนี้สามารถถูก override ได้ในคลาสลูก
- DerivedClass เราทำการ override เมทอด Print() ที่ถูกสืบทอดมาจาก BaseClass และให้มันพิมพ์ข้อความ "Hello from DerivedClass"
- SecondDerivedClass เราก็ทำการ override เมทอด Print() อีกครั้ง พิมพ์ข้อความ "Hello from SecondDerivedClass"
- เรียกใช้เมทอด Print() ของ SecondDerivedClass ผ่านอ็อบเจกต์ของ SecondDerivedClass (sdRef) จะพิมพ์ข้อความ "Hello from SecondDerivedClass" 



