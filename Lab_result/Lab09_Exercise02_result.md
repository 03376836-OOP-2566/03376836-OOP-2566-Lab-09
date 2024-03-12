## บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
![image](https://github.com/Sorawit255/03376836-OOP-2566-Lab-09/assets/144196505/ac2ebfc2-456e-4c19-bfd6-8c36a871e240)

## บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/Sorawit255/03376836-OOP-2566-Lab-09/assets/144196505/b016f9b6-b65a-44d8-b395-5160ad269a4a)

## อธิบายสิ่งที่พบในการทดลอง
### บรรทัดที่ 2 `BaseClass bcRef = (BaseClass) dcRef;` จะทำการนำ Obj ของตัวแปร dcRef มาสร้างใหม่เป็น Obj ของคลาส BaseClass แล้วเก็บไว้ในตัวแปร bcRef
### เมื่อเรียกใช้ dcRef.info() จะแสดง  "This is DerivedClass"
### เมื่อเรียกใช้ bcRef.info() จะแสดง  "This is DerivedClass" ที่ถูก override ในคลาสลูก (DerivedClass) ทำให้ผลลัพธ์เป็น "This is DerivedClass" 
