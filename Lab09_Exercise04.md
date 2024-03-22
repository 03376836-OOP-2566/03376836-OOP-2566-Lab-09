# Lab 9 Exercise 4

## Override overridden Method
![alt text](./Pictures/image02.png)
1.สร้าง console application project

```cmd
dotnet new console --name Lab09_Ex04
```
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/c64713a8-33d0-4d76-9cb5-34c83b621b09)

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
    public void Print()
    {
       System.Console.WriteLine("Hello from SecondDerivedClass");
    }
}
```
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/3fa1773e-ea3d-4b36-b4c0-22b1dfa10687)

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab09_Ex04
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/b9482b57-0e67-461e-bfc9-01efe2512202)
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/0daf1cf3-0c35-4460-89f2-acf32435eea5)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex04
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5

![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/f99e086a-ced0-486a-841b-de1e440d074c)

7.อธิบายสิ่งที่พบในการทดลอง

การทดลองนี้มีการสร้างอ็อบเจกต์ sdRef จากคลาส SecondDerivedClass และ bcRef จากคลาส BaseClass โดยใช้การแปลงชนิด (casting) sdRef ไปยัง BaseClass ด้วย (BaseClass) sdRef จากนั้นเมื่อเรียกใช้เมธอด Print() ของทั้ง sdRef และ bcRef จะแสดงข้อความ "Hello from SecondDerivedClass" ด้วย เนื่องจากเมธอด Print() ไม่ได้ถูกโอเวอร์ไรด์ในคลาส DerivedClass หรือ BaseClass แต่ถูกนำมาใช้โดยตรงจากคลาส SecondDerivedClass ซึ่งเป็นคลาสที่สืบทอดมาจาก DerivedClass และ BaseClass เราจะเห็นการแสดงผลของคำสั่งออกมาดังภาพด้านบน การบันทึกผลข้อที่ 5
