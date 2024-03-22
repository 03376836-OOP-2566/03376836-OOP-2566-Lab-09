# Lab 9 Exercise 1

## Polymorphism (virtual-override methods)

1.สร้าง console application project

```cmd
dotnet new console --name Lab09_Ex01
```
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/f531d548-f721-4b7e-8b79-92e738f0c351)

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
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/269aba04-a47e-4476-afb7-b1822acf7b46)

3.Build project โดยการใช้คำสั่ง

```cmd
dotnet build  Lab09_Ex01
```

ถ้ามีที่ผิดพลาดในโปรแกรม ให้แก้ไขให้ถูกต้อง

4.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/64562a6e-3468-4fff-9976-7b0a20ba5cb3)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex01
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/AnchisaPhetnoi/03376836-OOP-2566-Lab-09/assets/144197034/d56cac62-8537-4b3b-b394-0e3e89f4071b)

7.อธิบายสิ่งที่พบในการทดลอง

การทดลองนี้ เราสร้างคลาสชื่อ BaseClass และ DerivedClass โดย DerivedClass ได้สืบทอดจาก BaseClass และมีการโอเวอร์ไรด์เมทอด Info() ซึ่งถูกประกาศเป็นเมทอด virtual ใน BaseClass และ override ใน DerivedClass ในเมทอด Info() ของ BaseClass เรามีการแสดงข้อความ "This is BaseClass" และใน DerivedClass เรามีการแสดงข้อความ "This is DerivedClass" โดยในการทดลอง เราสร้างอ็อบเจกต์ของคลาส DerivedClass และ BaseClass ตามลำดับ และเรียกใช้เมทอด Info() ของทั้งคลาส ซึ่งจะแสดงข้อความที่ถูกโอเวอร์ไรด์ตามคลาสของอ็อบเจกต์ที่ถูกสร้างขึ้น ดังการแสดงผลดังภาพด้านบน ที่มีการแสดงผลออกมาเป็น 2 อย่างคือ  DerivedClass และตัว BaseClass 
