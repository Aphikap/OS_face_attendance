# Face Attendance Project

## Project Structure

```
face-attendance/
|
|-- docker-compose.yml          # ใช้รันบนเครื่องหลัก (Windows)
|
|-- backend/
|   |-- Dockerfile              # build backend image
|   |-- requirements.txt        # python dependencies
|   |-- api.py                  # Flask API (เรียก init_db ตอน start)
|   |-- database.py             # helper เปิด SQLite connection
|   |-- init_db.py              # สร้างตาราง DB (students, faces, attendance)
|   |-- data/
|   |   |-- attendance.db       # SQLite database (ถูกสร้างอัตโนมัติ)
|   |   |-- faces/              # (ยังว่าง) เก็บรูปหน้าที่ enroll
|
|-- frontend/
|   |-- index.html              # หน้าเว็บทดสอบ check-in / ดู attendance
|
|-- nginx/
|   |-- nginx.conf              # reverse proxy / serve frontend
```
"# OS_face_attendance" 
