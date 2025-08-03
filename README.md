# Project_Node.js+Express.js+EJS+ MongoDB
ระบบจัดการสินค้าแบบ Fullstack พื้นฐาน พัฒนาโดยใช้ Node.js และ Express.js ฝั่ง Backend และใช้ EJS แสดงผลฝั่ง Frontend พร้อมรองรับการอัปโหลดรูปภาพด้วย `multer`
---
## 🧰 การตั้งค่า / Packages ที่ใช้

```json
"dependencies": {
  "ejs": "3.1.10",
  "express": "5.1.0",
  "mongoose": "8.15.2",
  "multer": "2.0.1",
  "nodemon": "^3.1.10"
}
```

## ⚙️ Tech Stack

| เทคโนโลยี                | รายละเอียด                      |
| ------------------------ | ------------------------------- |
| **Node.js + Express.js** | ใช้เป็น Web Server และ Routing  |
| **MongoDB + Mongoose**   | จัดการฐานข้อมูลแบบ NoSQL        |
| **EJS**                  | Template Engine สำหรับแสดง HTML |
| **Multer**               | จัดการอัปโหลดรูปภาพ             |
| **Bootstrap / CSS**      | ใช้ตกแต่ง UI ผ่านไฟล์ static    |

## ชุดฐานข้อมูล
```
    - ทำการ import ไฟล์ productDB.product.json ไปใช้ใน MongoDB
    - เข้าไปในโฟลเดอร์ models->products.js
    - ทำการตั้งค่า/ตรวจเช็ก 'localhost:27017/productDB' ตามที่อยู่ใน MongoDB
```

## 📦 Features
```
    - แสดงรายการสินค้า (พร้อมรูปภาพ)
    - เพิ่มสินค้าใหม่ พร้อมอัปโหลดภาพ
    - ลบสินค้า
    - ดูรายละเอียดสินค้าทีละชิ้น
    - ใช้ MongoDB/Mongoose สำหรับเก็บข้อมูล
    - ใช้ EJS แสดงผลหน้า HTML
    - CSS แยกไฟล์ผ่าน `/public`
```


## 📁 Project Structure
```
project_node_js/
├── models/               # Mongoose Schema
│   └── product.js
├── routes/               # Routing
│   └── myrouter.js
├── views/                # ไฟล์ EJS Template
│   ├── index.ejs         # หน้าแสดงรายการ
│   ├── insert.ejs        # ฟอร์มเพิ่มสินค้า
│   ├── show.ejs          # แสดงรายละเอียดสินค้า
│   └── header.ejs        # Header แยกไว้เรียกใช้รวม
│   └── edit.ejs          # แก้ใขข้อมูล
│   └── tabledata.ejs     # แสดงข้อมูลในรูปแบบตาราง
├── public/               # ไฟล์ Static เช่น CSS, รูปภาพ
│   ├── css/              # ไฟล์ตกแต่ง
│   └── img/products/     # รูปสินค้าที่อัปโหลด
├── app.js                # จุดเริ่มต้นของแอป
└── package.json
```

## Usage(การใช้งาน)
```
🔹 แสดงสินค้าเข้าเว็บไซต์ที่ /
    จะแสดงรายการสินค้าทั้งหมดพร้อมรูปภาพ

🔹 เพิ่มสินค้าใหม่เข้าหน้า /insert
    กรอก name, price, size, description และเลือกรูปภาพกดปุ่ม "บันทึก"

🔹 ดูรายละเอียดสินค้า
    คลิกปุ่ม "เพิ่มเติม" หรือ "Read More" ข้อมูลจะแสดงจาก product._id ที่ query มาจาก MongoDB

🔹 ลบสินค้า
    ใช้ <form method="POST" action="/delete/:id"> มี confirm() ยืนยันก่อนลบจริง
    ข้อมูลจะถูกลบจาก MongoDB
```

# Run the server
```
node app.js
หรือใช้ nodemon เพื่อไม่ต้อง restart ทุกครั้ง
npx nodemon app.js
# หรือถ้าตั้ง script ไว้ใน package.json
npm start
```

# ✍️ ผู้พัฒนา
```
ชื่อ-นามสุก: เจริญ ศักดิ์เจริญชัยกุล 
อีเมล: jsaroen66@gmail.com
GitHub: github.com/JaroenGit
```


