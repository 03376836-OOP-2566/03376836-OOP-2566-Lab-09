## บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
![image](https://github.com/Sorawit255/03376836-OOP-2566-Lab-09/assets/144196505/b2c02434-10da-4530-9038-8b649c499c84)

## บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/Sorawit255/03376836-OOP-2566-Lab-09/assets/144196505/60958cec-182c-47e7-b409-fcf3c889ebe7)

## อธิบายสิ่งที่พบในการทดลอง
### เมื่อเรียกใช้ sdRef.Print(); จะแสดง "Hello from SecondDerivedClass" เนื่องจากเมธอด Print() ถูก override ในคลาส SecondDerivedClass
### เมื่อเรียกใช้ bcRef.Print(); จะแสดง "Hello from DerivedClass" เนื่องจากเมธอด Print() ถูก override ในคลาส DerivedClass
### bcRef.Print() ถูก override ในคลาส DerivedClass(bcRef ถูกสร้างจาก BaseClass ซึ่งในที่นี้ DerivedClass ถูกเรียกใช้งานเนื่องจาก bcRef ถูกอ้างอิงเป็น BaseClass ที่ไม่รู้จักเมธอดใหม่ที่ถูกประกาศใน SecondDerivedClass ดังนั้นจึงไม่เรียกใช้งาน Print() ใหม่ที่เมธอดของ SecondDerivedClass โปรแกรมจึงเลือกเรียกใช้งานเมธอด Print() ของ DerivedClass แทน ซึ่งก็คือ "Hello from DerivedClass")
