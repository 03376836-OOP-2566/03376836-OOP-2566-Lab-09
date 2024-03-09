# Lab 9 Exercise 1

## Polymorphism (virtual-override methods)

1.สร้าง console application project

```cmd
dotnet new console --name Lab09_Ex01
```

2.เปลี่ยน code ให้เป็นดังต่อไปนี้

```cs
Student student1 = new Student();
student1.Name = "Somchai";
System.Console.WriteLine($"student1 name = {student1.Name}");

var student2 = new Student();
student2.Name = "Sompong";
System.Console.WriteLine($"student2 name = {student2.Name}");

class Person
{
    private string name = string.Empty;
    public string Name
    {
        get { return name; }
        set { name = value; }
    }
}

class Student:Person
{

}
```

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab09_Ex01
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex01
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5

7.อธิบายสิ่งที่พบในการทดลอง
