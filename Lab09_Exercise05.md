# Lab 9 Exercise 5

## Override with `new` keyword
![alt text](./Pictures/image03.png)
1.สร้าง console application project

```cmd
dotnet new console --name Lab09_Ex05
```
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/86d079a4-4360-4b46-856d-c04349afa2c5)

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
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/e4b0731f-5eae-4745-aafe-6cbf37eb9c41)

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab09_Ex05
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/e262e86e-a38b-4539-b33e-ddb9862a4e02)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex05
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/9a0f9ebc-f5b2-4dce-9fb6-b2a088093b22)

7.อธิบายสิ่งที่พบในการทดลอง

จากการทดลองนี้มีการสร้างอ็อบเจกต์ sdRef จากคลาส SecondDerivedClass และ bcRef จากคลาส BaseClass โดยใช้การแปลงชนิด (casting) sdRef ไปยัง BaseClass ด้วย (BaseClass) sdRef จากนั้นเมื่อเรียกใช้เมธอด Print() ของทั้ง sdRef และ bcRef จะแสดงข้อความ "Hello from SecondDerivedClass" ด้วย เนื่องจากเมธอด Print() ถูกโอเวอร์ไรด์ใหม่ (new override) ในคลาส SecondDerivedClass ซึ่งทำให้เมธอดของคลาสลูกถูกเรียกใช้ในที่นี้ เราจะเห็นผลการทดลองดังภาพด้านบน
