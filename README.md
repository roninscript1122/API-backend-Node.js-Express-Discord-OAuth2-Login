# API backend (Node.js + Express) สำหรับ Discord OAuth2 Login

โปรเจกต์นี้เป็นตัวอย่าง **API Backend** ที่ทำด้วย **Node.js + Express** เพื่อรองรับการ Login ผ่าน **Discord OAuth2**  
สามารถนำไปใช้คู่กับ **Frontend (เช่น Vite/React)** ได้เลย

---

## 🔧 Features
- Login ด้วย Discord OAuth2
- ใช้ JWT เก็บ session
- รองรับการเรียกจาก Frontend (CORS)
- Cookie-based authentication
- โครงสร้างง่าย เหมาะสำหรับทำโปรเจกต์จริง

---

## 📦 Dependencies
- express
- dotenv
- mysql2 (เชื่อมฐานข้อมูล ถ้าต้องการเก็บ user)
- discord-oauth2
- cors
- cookie-parser
- jsonwebtoken

---

## 📂 โครงสร้างโปรเจกต์ (Project Structure)
```bash
discord-oauth2-backend/
│
├─ src/
│ ├─ config/
│ │ └─ db.js # ตั้งค่าการเชื่อมฐานข้อมูล
│ │
│ ├─ middlewares/
│ │ └─ require-auth.js # middleware สำหรับตรวจสอบ authentication
│ │
│ ├─ modules/
│ │ └─ auth/
│ │ ├─ auth.controller.js # จัดการ logic ของ auth
│ │ ├─ auth.routes.js # route สำหรับ auth
│ │ ├─ auth.service.js # service สำหรับ auth
│ │ ├─ discord.auth.js # OAuth2 Discord login logic
│ │ └─ token.js # จัดการ JWT token
│ │
│ └─ appserver.js # ไฟล์หลักของเซิร์ฟเวอร์
│
├─ .env # Environment variables
├─ .gitignore # ป้องกันไฟล์ที่ไม่ต้องการ push
├─ package.json
└─ README.md
```

---
## วิธีสร้าง Discord Application (Step by Step)

### 1️⃣ เข้า Discord Developer Portal
- เปิดเบราว์เซอร์ไปที่: [Discord Developer Portal](https://discord.com/developers/applications)
- คุณจะเห็นหน้า **Applications** ของคุณ  

**แนะนำ:** capture รูปภาพหน้าจอทั้งหมดของ Developer Portal  
![Step 1 - Developer Portal](images/step1-developer-portal.png)


---

💡 **Tips:**  

1. สร้างโฟลเดอร์ `images/` ในโปรเจกต์ เพื่อเก็บ screenshot  
2. ชื่อไฟล์ภาพให้สอดคล้องกับ step เช่น `step1-developer-portal.png`  
3. Markdown จะ render รูปภาพพร้อมคำอธิบาย และอ่านง่ายบน GitHub  

---

ถ้าคุณต้องการ ผมสามารถทำ **ตัวอย่าง README.md แบบสมบูรณ์รวมทั้ง Project Structure + Discord OAuth2 Login + Step by Step รูปภาพ** ให้พร้อมอัปขึ้น GitHub ได้เลย  

คุณอยากให้ผมทำไหม?



---

## 📖 ขั้นตอนการสร้างโปรเจกต์ตั้งแต่เริ่มต้น

### 1. สร้างโฟลเดอร์โปรเจกต์
```bash
mkdir discord-oauth2-backend
cd discord-oauth2-backend
```

### 2. สร้าง Node.js Project
```bash
npm init -y
```

### 3. ติดตั้ง Dependencies
```bash
npm install express dotenv mysql2 discord-oauth2 cors cookie-parser jsonwebtoken
```

### 4. สร้างไฟล์ src/appserver.js
ใส่โค้ดตัวอย่างนี้ลงไป:
```bash
code example
```
