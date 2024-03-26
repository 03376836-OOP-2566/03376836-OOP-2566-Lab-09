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
![image](https://github.com/VisawaPRO/03376836-OOP-2566-Lab-09/assets/144195555/9c34d4f4-299e-4f24-b3e1-b516104b9766)
### สามารถ Build ได้ เพราะ virtual: ใช้บอกว่าเมทอดสามารถถูกโอเวอร์ไรด์ได้ในคลาสที่สืบทอด คือ Info override: ใช้ในคลาสที่สืบทอดเพื่อโอเวอร์ไรด์เมทอดที่ถูกประกาศเป็น virtual ในคลาสฐาน
5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex01
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/VisawaPRO/03376836-OOP-2566-Lab-09/assets/144195555/bc81e0de-8084-4776-9e71-7bf7bd05390d)
### สามารถ Run ได้ เพราะ Info ถูกประกาศเป็น virtual สามารถถูก override ได้ในคลาสที่สืบทอด
7.อธิบายสิ่งที่พบในการทดลอง
### โปรแกรมจะแสดงผล
### This is DerivedClass
### This is BaseClass
