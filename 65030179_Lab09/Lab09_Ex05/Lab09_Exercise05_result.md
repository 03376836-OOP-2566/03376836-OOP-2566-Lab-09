# Exercise 5.1
![Ex5 1](https://github.com/65030179179Pattarapon/03376836-OOP-2566-Lab-09/assets/144198506/a87ecd00-41f5-41fe-9f1d-b73e6381292e)

# Exercise 5.2
![Ex5 2](https://github.com/65030179179Pattarapon/03376836-OOP-2566-Lab-09/assets/144198506/befc5ba5-e305-40fe-ab95-7cbff8f9e107)

##
#### ในการทดลองนี้ เราสร้างอ็อบเจกต์ sdRef จากคลาส SecondDerivedClass และทำการแปลงชนิดของ sdRef เป็น BaseClass โดยใช้การ casting (BaseClass) sdRef ซึ่ง BaseClass เป็นคลาสฐานของ SecondDerivedClass แต่เนื่องจากเมธอด Print() ใน SecondDerivedClass ไม่ได้รับการจับคู่ (override) กับเมธอด Print() ใน BaseClass หรือ DerivedClass จึงไม่สามารถเรียกใช้ได้ผ่านทางตัวแปร bcRef ที่ถูกแปลงเป็น BaseClass โดยการแปลงชนิด ผลลัพธ์ที่พิมพ์ออกทางหน้าจอจะเป็น "Hello from SecondDerivedClass" สำหรับ sdRef.Print() และ "Hello from BaseClass" สำหรับ bcRef.Print() โดยใช้การเรียกเมธอดที่เป็นของ BaseClass ที่ถูกแปลงแล้ว
