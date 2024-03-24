# Exercise 4.1
![Ex4 1](https://github.com/65030179179Pattarapon/03376836-OOP-2566-Lab-09/assets/144198506/664820fa-0b1f-46be-9156-ac875131a1f4)

# Exercise 4.2
![Ex4 2](https://github.com/65030179179Pattarapon/03376836-OOP-2566-Lab-09/assets/144198506/f2c6a9fc-9a85-4e7d-85dd-00d454ef7b47)

##
#### ในการทดลองนี้ เราสร้างอ็อบเจกต์ sdRef จากคลาส SecondDerivedClass และทำการแปลงชนิดของ sdRef เป็น BaseClass โดยใช้การ casting (BaseClass) sdRef ซึ่ง BaseClass เป็นคลาสฐานของ SecondDerivedClass แต่เนื่องจากเมธอด Print() ใน SecondDerivedClass ไม่ได้รับการจับคู่ (override) กับเมธอด Print() ใน BaseClass หรือ DerivedClass จึงไม่สามารถเรียกใช้ได้ผ่านทางตัวแปร bcRef ที่ถูกแปลงเป็น BaseClass โดยการแปลงชนิด ดังนั้น ผลลัพธ์ที่พิมพ์ออกทางหน้าจอจะเป็น "Hello from SecondDerivedClass" สำหรับ sdRef.Print() แต่สำหรับ bcRef.Print() จะไม่สามารถเรียกใช้เมธอด Print() ใน SecondDerivedClass ได้ ซึ่งทำให้โปรแกรมไม่สามารถคอมไพล์ได้ถูกต้องโดยมีข้อผิดพลาดที่เกิดขึ้นในบรรทัดที่ bcRef.Print() นั่นเอง




