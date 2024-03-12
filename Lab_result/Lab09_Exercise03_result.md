## บันทึกผลที่ได้จากการรันคำสั่งในข้อ 3
![image](https://github.com/Sorawit255/03376836-OOP-2566-Lab-09/assets/144196505/1892abd5-aa71-45be-969d-e9cd9bdbe75e)

## บันทึกผลที่ได้จากการรันคำสั่งในข้อ 5
![image](https://github.com/Sorawit255/03376836-OOP-2566-Lab-09/assets/144196505/1afe4fb1-67fe-4b0f-9473-e1af2b798127)

## อธิบายสิ่งที่พบในการทดลอง
### โค้ดนี้เกี่ยวกับ Override overridden Method
### บรรทัดที่ 2 `BaseClass bcRef = (BaseClass) sdRef;` จะทำการนำ Obj ของตัวแปร sdRef มาสร้างใหม่เป็น Obj ของคลาส BaseClass แล้วเก็บไว้ในตัวแปร bcRef
### เมื่อเรียกใช้ sdRef.info() จะแสดง  "Hello from SecondDerivedClass" 
### เมื่อเรียกใช้ bcRef.info() จะแสดง  "Hello from SecondDerivedClass"  ที่ถูก override ในคลาสลูก (SecondDerivedClass) ทำให้ผลลัพธ์เป็น "Hello from SecondDerivedClass" 
