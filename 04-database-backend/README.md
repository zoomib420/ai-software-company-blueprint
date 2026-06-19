# 04 — Database & Backend

## เป้าหมาย

มีแนวทาง backend/database เดียวที่คุ้นเคยและใช้ซ้ำได้กับงานลูกค้าส่วนใหญ่ แทนการเลือกใหม่ทุกครั้ง
เน้นความเร็วในการส่งมอบและความง่ายในการ debug มากกว่าความสมบูรณ์แบบทางสถาปัตยกรรม

## สิ่งที่ต้องเรียน

- PostgreSQL พื้นฐาน + เครื่องมือจัดการที่เร็ว เช่น Supabase (มี Auth + Storage + REST/Realtime มาในตัว)
- การออกแบบ data model พื้นฐานสำหรับงาน SME: contacts/leads, orders/items, schedule/bookings
- การออกแบบ REST API ง่ายๆ (CRUD) ที่ frontend เรียกใช้ได้ตรงไปตรงมา
- การเชื่อมระบบเดิมที่ไม่มี API (ทักษะที่มีอยู่แล้วจาก Schedule Automator) เข้ากับฐานข้อมูลใหม่
- Backup/migration พื้นฐาน — กันข้อมูลลูกค้าหายตอนแก้ schema

## โปรเจกต์ที่ต้องทำ

1. ตั้ง Supabase project ต้นแบบ 1 ชุดที่ใช้เป็น "ฐาน" สำหรับ demo Mini CRM/Mini ERP ใน stage 05–06
2. สร้าง CRUD API demo เล็กๆ (เช่น ระบบจองคิว/ระบบสต๊อกสินค้าง่ายๆ) เพื่อฝึกรูปแบบที่จะใช้ซ้ำกับลูกค้าจริง

## Checklist

- [ ] เลือกผู้ให้บริการ DB/backend หลัก (แนะนำ Supabase) แล้วบันทึกเหตุผลใน [DECISIONS.md](../DECISIONS.md)
- [ ] มี data model ต้นแบบสำหรับ leads/contacts ที่ใช้ต่อใน 05-mini-crm ได้
- [ ] มี data model ต้นแบบสำหรับ inventory/scheduling ที่ใช้ต่อใน 06-mini-erp ได้
- [ ] มีตัวอย่าง API CRUD ที่ frontend จาก [03-web-app-foundation](../03-web-app-foundation/) เรียกได้จริง
- [ ] รู้วิธี backup/restore ฐานข้อมูลก่อนเริ่มงานลูกค้าจริงรายแรก

## งานที่สามารถรับได้ตอนนี้

- เพิ่มฐานข้อมูลให้ระบบที่ลูกค้าทำด้วย spreadsheet อยู่แล้วแต่เริ่มไม่พอ
- ต่อ API ให้ฟอร์ม/เว็บลูกค้าบันทึกข้อมูลเข้าฐานข้อมูลจริงแทน Sheet
- งานย้ายข้อมูลจากระบบเดิม (ERP/ระบบเก่า) เข้าฐานข้อมูลใหม่ (ใช้ทักษะ reverse engineering ที่มีอยู่แล้ว)

## สิ่งที่ยังไม่ต้องทำ

- ❌ Microservices หรือ message queue — เกินความจำเป็นสำหรับงาน SME ขนาดนี้
- ❌ Self-host database server เอง — ใช้ managed service (Supabase/อื่นๆ) ประหยัดเวลาดูแลระบบ
- ❌ ออกแบบ schema ให้ "รองรับทุกอนาคต" ตั้งแต่แรก — ออกแบบให้พอใช้กับ Mini CRM/ERP ปัจจุบัน ขยายทีหลังตามจริง
