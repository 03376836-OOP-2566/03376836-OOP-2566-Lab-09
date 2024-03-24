# Exercise 1.1
![Ex1 1](https://github.com/65030179179Pattarapon/03376836-OOP-2566-Lab-09/assets/144198506/c3ffae43-4648-460e-bb56-b6ea732998a9)

# Exercise 1.2
![Ex1 2](https://github.com/65030179179Pattarapon/03376836-OOP-2566-Lab-09/assets/144198506/fee7b0b5-ec8b-477a-8d4f-50a6238055fe)

##
#### ในการทดลองนี้ เราสร้างคลาส BaseClass และ DerivedClass โดย DerivedClass สืบทอดจาก BaseClass ซึ่ง Info() เป็นเมธอดเสมือนที่ถูกสร้างขึ้นใน BaseClass และถูกเขียนทับใน DerivedClass ซึ่งเราใช้คีย์เวิร์ด virtual ใน BaseClass เพื่อให้เป็นเมธอดที่สามารถถูกซ่อนแทนได้ และใช้คีย์เวิร์ด override ใน DerivedClass เพื่อบอกว่าเรากำลังทับเมธอดจาก BaseClass ดังนั้น เมื่อเรียกใช้ Info() ผ่านอ็อบเจกต์ของ DerivedClass จะเรียกใช้เมธอดที่ถูกทับใน DerivedClass และเมื่อเรียกใช้ผ่านอ็อบเจกต์ของ BaseClass จะเรียกใช้เมธอดใน BaseClass ผลลัพธ์ที่พิมพ์ออกทางหน้าจอจะเป็น "This is DerivedClass" สำหรับ dcRef.Info() และ "This is BaseClass" สำหรับ bcRef.Info() ตามลำดับ ซึ่งแสดงให้เห็นถึงการทับเมธอดในการสืบทอดและพฤติกรรมของเมธอดเสมือนในภาษา C#
