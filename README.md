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

ติดตั้งทั้งหมด:
```bash
npm install express dotenv mysql2 discord-oauth2 cors cookie-parser jsonwebtoken
