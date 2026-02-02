# Tutorial-5.2-Embedded-Systems-and-IoT-Firebase & SQL (MariaDB)

<h2>การส่งค่าเข้าฐานข้อมูล</h2>
<h3>Objectives</h3>

1. ส่งค่าเข้าฐานข้อมูล Firebase ได้
2. ส่งค่าเข้าฐานข้อมูล MySQL ได้

<h3>Hardware</h3>

1.	เซ็นเซอร์ตามต้องการ        	      1
2.	ESP32                           1
3.	Breadboard                      1
5.	Computer	                      1
6.	microUSB	                      1 

<h3>Software</h3>h3>

1. Arduino IDE
--------------------
<h3>Instruction</h3>

<h2>ส่งค่าขึ้นฐานข้อมูล Firebase</h2>

1. ตั้งค่า Firebase โดยทำตามขั้นตอนในลิงค์นี้ https://docs.google.com/document/d/1LjWkR9mvH9aqHAJQuuZbgV3OkncwM3AxFvffaiNQIKk/edit?usp=sharing
2. คัดลอกโค้ดในโฟลเดอร์ lab6 > Lab_6.ino
3. ติดตั้ง Firebase Library โดยดูขั้นตอนจากลิงค์เดียวกัน
4. เปลี่ยนค่า API-KEY และ Database URL ให้เป็นของตัวเอง
5. ทำการอัพโหลดโค้ดและดูผลลัพธ์บน Firebase จะต้องขึ้นค่า int และ float
6. ส่งค่าจริงจากเซ็นเซอร์ Temperature หรือ Ultrasonic ขึ้นไปยัง Firebase โดยใช้โค้ดเซ็นเซอร์จากแลปก่อนหน้า

หมายเหตุ
หากพบ error ขณะทำการ upload เกี่ยวกับ SD.h และ unsupported board ให้ดำเนินการดังนี้
1. ไปที่ File -> Preferences -> Aditional boards manager URLs
2. คัดลอก URL นี้ไปใส่ในช่อง boards manager URLs >> https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
3. ติดตั้ง library ของบอร์ดโดยไปที่ Tools -> Board -> Boards Manager
4. ค้นหา "esp32" และติดตั้งเวอร์ชัน 2.0.1


--------------------

<h2>ส่งค่าขึ้นฐานข้อมูล SQL</h2>

1. ดูวิธีการสร้าง database ที่ลิงค์ https://www.youtube.com/watch?v=F5T8isU13bU (ดูถึงแค่นาทีที่ 20) เนื้อหาในคลิปจะเป็นการใช้งาน 000webhost แต่ให้นักศึกษาใช้ infinityFree (หรือ host อื่นๆ) แทน
2. เขียนโปรแกรมฝั่ง cloud โดยดาวน์โหลดไฟล์ con_db.php, data_receive.php ได้ที่โฟลเดอร์
3. นำไฟล์ con_db.php และ data_receive.php ไปใส่ไว้ในโฟลเดอร์ htdocs บน infinityFree
4. เปลี่ยนค่าการเชื่อมต่อข้อมูลในไฟล์ con_db.php ให้เป็นข้อมูลของตัวเอง
5. เขียนโปรแกรมฝั่ง esp32 โดยดาวน์โหลดไฟล์ lab_7.ino ได้ที่โฟลเดอร์ lab7
6. เปลี่ยนค่า WiFi และ servername ให้เป็นของตัวเอง
6. ส่งค่าจริงจากเซ็นเซอร์ Temperature หรือ Ultrasonic ขึ้นไปยัง Firebase โดยใช้โค้ดเซ็นเซอร์จากแลปก่อนหน้า
7. อัพโหลดโค้ดและดูค่าที่ถูกส่งเข้าไปยังฐานข้อมูล SQL บน pypMyAdmin

เสริม: ดูวิธีการนำค่าขึ้นฐานข้อมูลที่ลิงค์ https://www.youtube.com/watch?v=C_LXWEQAy5w สามารถใช้ได้กับ infinityFree



