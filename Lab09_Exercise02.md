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
![image](https://github.com/65030121natthamon/03376836-OOP-2566-Lab-09/assets/144195611/2a42a708-5ace-4e46-b663-a154aae23cb5)

5.Run project โดยการใช้คำสั่ง

```cmd
dotnet run --project Lab09_Ex02
```

6.บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/65030121natthamon/03376836-OOP-2566-Lab-09/assets/144195611/874a214a-02cf-41b9-bc96-839c91a931c3)

7.อธิบายสิ่งที่พบในการทดลอง
- มีการใช้virtual-override methodsตั้งแต่การสร้างคลาส BaseClassและDevivedClass
- virtual-override methods ได้ถูกใช้งานในโปรแกรมดังกล่าวตอนที่เราประกาศเมทอด Info() ในคลาส BaseClass เป็น virtual และ override เมทอด Info() ในคลาส DerivedClass ทำให้สามารถเปลี่ยนแปลงพฤติกรรมของเมทอด Info() จากคลาสแม่ให้กลายเป็นเมทอดใหม่ในคลาสลูกได้
