# GUARDIAN PBVS — Risk Intelligence

เว็บไซต์ React/Vite แบบ static สำหรับเผยแพร่ด้วย GitHub Pages

## ใช้งานในเครื่อง

```bash
npm install
npm run dev
```

เปิด URL ที่ Vite แสดงใน terminal

## Build ตรวจสอบก่อน Deploy

```bash
npm run build
npm run preview
```

## Deploy บน GitHub Pages

1. สร้าง GitHub repository ใหม่ แล้วอัปโหลดไฟล์ทั้งหมดในโฟลเดอร์นี้ไปยัง branch `main`
2. ไปที่ **Settings → Pages**
3. ตั้งค่า **Source: GitHub Actions**
4. Push ใหม่อีกครั้ง หรือกด **Actions → Deploy to GitHub Pages → Run workflow**
5. GitHub จะสร้าง URL สำหรับเว็บไซต์ให้อัตโนมัติ

ไฟล์ `.github/workflows/deploy.yml` จะ build และ deploy ทุกครั้งที่ push ไปยัง `main` โดยไม่ต้องตั้งค่า Build command ใน Pages เพิ่มเติม

## หมายเหตุ

ไฟล์รูปภาพถูกย้ายมาไว้ใน `src/assets` แล้ว เพื่อไม่ให้การ deploy พึ่งพา Manus storage เดิม และตั้งค่า Vite เป็น `base: "./"` เพื่อให้ใช้งานได้ทั้ง repository URL และ custom domain
