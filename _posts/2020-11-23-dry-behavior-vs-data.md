---
layout: post
title: DRY ใช้กับ Behavior ไม่ใช้กับ Data
---

ผมว่าเราคงได้ยินคำว่า DRY ( Don't repeat your self ) บางครั้งทำให้เวลาเรา ต้องการ response เราใช้ struct ตัวเดียวกับ ที่ใช้ db เพราะเราทำตามข้อกำหนดนี้คือ เรา DRY

แต่ผมศึกษามาคร่าวๆนั้น DRY ใช้กับ พฤติกรรม ไม่ใช่กับ ข้อมูล  หมายถึงว่า ถ้าเรามี code ที่ทำงานเหมือนกัน สักสามที่ เราควรทำเป็น function สะ

แต่กับ data จากที่ผมศึกษามาคร่าวๆ ใน go เราอาจจะเคยเจอ

```go
type User struct {
  Name string `bson:"name" json:"name"`
  Email string `bson:"email" json:"email"`
}
```
แบบนี้เราสามารถใช้ struct ตัวนี้กับ mongo และ กับ json response ได้ แต่จริงๆ แล้วเราควรแยกกัน

```go
type UserResponse struct {
   Name string  `json:"name"`
   Email string `json:"email"`
}

type UserModel struct {
   Name string  `bson:"name"`
   Email string `bson:"email"`
}
```

ข้อดีคือ เวลาเรามี field ที่ไม่อยากแสดงออกทาง json เราก็ทำได้ แค่เอา field นั้นออก เช่น

```go
type UserResponse struct {
   Name string  `json:"name"`
}
```
แบบนี้จะดีกว่ามาก
