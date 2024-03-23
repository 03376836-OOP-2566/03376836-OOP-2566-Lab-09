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
![image](https://github.com/VisawaPRO/03376836-OOP-2566-Lab-09/assets/144195555/f13b794c-0161-41b3-8134-46ee77366a06)
### สามารถ Build ได้ เพราะ มีการสร้างคลาสที่สืบทอด จากคลาสอื่น ๆ และโอเวอร์ไรด์เมทอดในคลาสที่สืบทอดนั้น
5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex02
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/VisawaPRO/03376836-OOP-2566-Lab-09/assets/144195555/a4ccaa56-9743-4ddf-a069-bd9a30d86b5e)
### สามารถ Run ได้ เพราะ dcRef.Info() จะเรียกใช้เมทอด Info() จากคลาสที่สืบทอด (DerivedClass) และ bcRef.Info() จะเรียกใช้เมทอด Info() จากคลาสฐาน (BaseClass)
7.อธิบายสิ่งที่พบในการทดลอง
### โปรแกรมจะแสดงผล
### This is DerivedClass
### This is DerivedClass
