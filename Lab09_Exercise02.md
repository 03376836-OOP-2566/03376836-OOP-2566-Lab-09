# Lab 9 Exercise 2

## virtual-override methods

1.สร้าง console application project

```cmd
dotnet new console --name Lab09_Ex02
```
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/4e1f11f9-ad90-4161-952a-fc58ff31da3f)

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
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/433e99da-eb53-436e-9fcc-5b0430d0b14a)

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab09_Ex02
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/8c9007a0-057f-41d4-a529-14398082c88b)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex02
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/afcb05ae-f930-4c70-8e34-19e7e7892120)

7.อธิบายสิ่งที่พบในการทดลอง

จากการทดลอง การทดลองนี้เริ่มจากการสร้างอ็อบเจกต์ dcRef จากคลาส DerivedClass และอ็อบเจกต์ bcRef จากคลาส BaseClass โดยการใช้การแปลงชนิด (casting) dcRef ไปยัง BaseClass โดยการใช้ (BaseClass) dcRef จากนั้นเมื่อเรียกใช้เมธอด Info() ของทั้ง dcRef และ bcRef จะแสดงข้อความ "This is DerivedClass" ด้วย เนื่องจากว่าเมธอด Info() ได้ถูกโอเวอร์ไรด์ในคลาส DerivedClass ทำให้เมธอดที่ถูกเรียกใช้เป็นเมธอดของ DerivedClass แทนที่ของ BaseClass ตามที่ได้กำหนดในการทดลอง จะเห็นการแสดงผล ดังภาพด้านบน
