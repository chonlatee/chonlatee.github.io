---
layout: post
title: การใช้ interface กับ oop design pattern ใน go
---

ช่วงนี้พยายามเรียนรู้เรื่อง oop design pattern ใน golang ก็เลยพอทราบได้ว่า oop design pattern นั้น ใช้ interface เยอะมาก

ไม่ว่าจะเป็น bridge pattern, adapter pattern, command pattern, optional pattern  และ design pattern นั้นก็เพิ่มความ complex ให้กับ code พอสมควร

ก็เลยมานั่งคิดว่า ตอนที่เราจะเขียน program จริงๆ นั้น เราต้องมาคำนึงถึงตรงนี้มั้ยนะ  แต่คิดไปคิดมามันก็คงต้องคำนึงถึงแหละ ไม่งั้นอาจจะทำให้ code มัน extend ไม่ค่อยได้

หรืออาจจะเป็นเพราะว่า ภาษาอื่นๆ ที่ไม่ใช่ go นั้น มันต้องประการ class a implement interface b แนวๆ นี้เลยทำให้ต้องคิดก่อนเขียนกันนะ

แต่ go ไม่ต้อง ผมก็เลยคิดว่า จริงๆ แล้วถ้าเขียน go อาจจะไม่ต้องคำนึงถึง oop design pattern ขนาดนั้นหรือเปล่านะ

แต่ก็นั้นแหละ ผมเองก็ไม่เซียน oop, design pattern อะไรพวกนี้เท่าไหร่ บอกไม่ได้เลย

แต่สิ่งหนึ่งที่บอกได้เลยคือ  รู้เรื่อง oop design pattern ทำให้เราเขียน code ดีขึ้นแน่นอน
