# หัวข้อการเรียนรู้  ESP32-IDF-Project

1. ESP32 Project

ESP32 project เป็น folder ที่รวมไฟล์ต่างๆ ที่ใช้งานร่วมกันเพื่อสร้าง  binary code ที่รันบน ESP32 ได้ ซึ่งไฟล์เหล่านั้นอาจจะเป็นได้ทั้ง Source code, header file, script และอื่น ๆ  รวมถึงไฟล์ที่เกิดจากการ build ของ toolchain ด้วย 

โดยทั่วไปแล้ว การ build ของโปรเจคที่มี source code เป็นภาษาซี จะมีกระบวนการที่เรียกว่าการคอมไพล์ (โดย compiler) ทำหน้าที่แปลง source code  เป็น object code แต่จะยังไม่สามารถรันบน ESP32 ได้โดยตรง จะต้องมีการเชื่อม (โดย Linker) เข้ากับ object code จาก source files อื่น ๆ รวมถึง object code ใน Library เสียก่อน จากนั้นจะนำ object code ที่รวมกันทั้งหมดมาจัดเรียง (relocated) จนกลายเป็น Application แล้วนำไปวางในหน่วยความจำของ ESP32 ตาม script ที่ระบุตำแหน่งของส่วนต่าง ๆ ของ Application (เรียกว่าการ upload) ซึ่งกระบวนการทั้งหมดนั้นจะถูกดำเนินการโดย toolchain อย่างอัตโนมัติ 


![Alt text](image.png)

เพื่อให้ toolchain ต่างๆ ทำงานได้อย่างถูกต้อง เราต้องรู้โครงสร้างของโฟลเดอร์ที่เก็บไฟล์ต่าง ๆ และการเชียนรายละเอียดในไฟล์ script ที่ทำหน้าที่ควบคุมการ build ทั้งหมด ไม่ว่าจะเป็นตำแหน่งที่เก็บ source code, ตำแหน่งของไฟล์ header เงื่อนไขต่างๆ ในการ build  ซึ่งโปรแกรมที่ตอยดำเนินการตระเตรียมสิ่งต่างๆ จนนำไปสู่การ build ได้สำเร็จนั้นเรียกว่า Ninja builder 

2. Folder structure

![](Pictures/Slides/Learning-topic-ESP32-IDF-Project-02.PNG)


![](Pictures/Slides/Learning-topic-ESP32-IDF-Project-03.PNG)


![](Pictures/Slides/Learning-topic-ESP32-IDF-Project-04.PNG)


![](Pictures/Slides/Learning-topic-ESP32-IDF-Project-05.PNG)


![](Pictures/Slides/Learning-topic-ESP32-IDF-Project-06.PNG)


![](Pictures/Slides/Learning-topic-ESP32-IDF-Project-07.PNG)


![](Pictures/Slides/Learning-topic-ESP32-IDF-Project-08.PNG)


![](Pictures/Slides/Learning-topic-ESP32-IDF-Project-09.PNG)

