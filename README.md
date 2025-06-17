# Project_Node.js+Express.js+EJS+ MongoDB
ระบบจัดการสินค้าแบบ Fullstack พื้นฐาน ใช้เทคโนโลยี Express, MongoDB, EJS และรองรับการอัปโหลดรูปภาพผ่าน `multer`
การตั้งค่า/ติดตั้งpackagesโปรเจกต์ Node.js
   - ejs: 3.1.10,
   - express: 5.1.0
   - mongoose": 8.15.2
   - multer: 2.0.1
   - nodemon: "^3.1.10
------------------------------------------------    
## ⚙️ Tech Stack
- **Node.js** + **Express.js** -->ใช้เป็น server  
- **MongoDB** + **Mongoose** -->ใช้ในการจัดการเกี่ยวกับฐานข้อมูล
- **EJS** --> (template engine) ใช้แสดงผลในรูปแบบของ HTML
- **Multer** --> (จัดการไฟล์ภาพ) ใช้เพื่อสามารถบันทึกข้อมูลภาพ และนามสกุลไฟล์ภาพ
- **Bootstrap / Custom CSS** (สำหรับ UI) --> ใช้หรับการตกแต่งไฟล์ .HTML หรือ.ejs
------------------------------------------------
📦 Features
    - แสดงรายการสินค้า (พร้อมรูปภาพ)
    - เพิ่มสินค้าใหม่ พร้อมอัปโหลดภาพ
    - ลบสินค้า
    - ดูรายละเอียดสินค้าทีละชิ้น
    - ใช้ MongoDB/Mongoose สำหรับเก็บข้อมูล
    - ใช้ EJS แสดงผลหน้า HTML
    - CSS แยกไฟล์ผ่าน `/public`
------------------------------------------------
## 📁 Project Structure
project_node_js/
├── models/ # Mongoose schema
│ └── product.js
├── routes/ # Express route handler
│ └── myrouter.js
├── views/ # EJS templates
│ ├── index.ejs
│ ├── show.ejs
│ ├── insert.ejs
│ └── header.ejs
├── public/ # Static files
│ ├── css/
│ └── img/products/ # Uploaded images
├── app.js # Main application file
└── package.json
------------------------------------------------
## Usage(การใช้งาน)

🔹 แสดงสินค้า
หน้า / จะแสดงสินค้าทั้งหมด

รูปภาพจะโหลดจาก /public/img/products

🔹 เพิ่มสินค้าใหม่
เปิดหน้า /insert

กรอก name, price, size, description และเลือกรูปภาพ

กด "บันทึก"

🔹 ดูรายละเอียดสินค้า
คลิก "เพิ่มเติม" ที่แต่ละสินค้า

🔹 ลบสินค้า
มีปุ่ม "ลบ" พร้อมยืนยันก่อนส่ง POST ไปยัง /delete/:id
------------------------------------------------
# Run the server
node app.js
# หรือใช้ nodemon
npx nodemon app.js หรือ npm star
