# 05 — Mini CRM

## เป้าหมาย

แปลง Intake Pilot (ที่มีอยู่แล้ว: AI chatbot รับลูกค้าผ่าน LINE/เว็บ → ส่งข้อมูลเข้า Notion) ให้กลายเป็น
"Mini CRM" ที่เป็นเทมเพลตขายซ้ำได้กับลูกค้าหลายราย ไม่ใช่ทำใหม่จากศูนย์ (ดู [DECISIONS.md](../DECISIONS.md) ADR-0003)

**อย่าเริ่ม stage นี้แบบจริงจังก่อนมีลูกค้าจริงขอ** — ใช้ Intake Pilot ตัวเดิมขายงานไปก่อนใน
[01-first-client](../01-first-client/)

## สิ่งที่ต้องเรียน

- พื้นฐานโดเมน CRM: lead → contact → pipeline stage → follow-up → ปิดงาน/ปิดการขาย
- Kanban UI pattern สำหรับ pipeline (drag-and-drop ระหว่าง stage)
- การแจ้งเตือน follow-up อัตโนมัติ (เช่น ลูกค้าเงียบ 3 วัน → เตือนเจ้าของธุรกิจ)
- ความแตกต่างระหว่าง "ใช้ Notion เป็น backend" (เร็ว ขายได้ทันที) กับ "มี database ของตัวเอง" (จาก
  [04-database-backend](../04-database-backend/)) — และเมื่อไหร่ควรย้ายจากแบบแรกไปแบบหลัง

## โปรเจกต์ที่ต้องทำ

1. Generalize Intake Pilot: แยกส่วน "AI สัมภาษณ์ลูกค้า" ออกจากส่วน "เก็บข้อมูลเฉพาะธุรกิจเดิม" ให้ config
   คำถาม/หมวดงานได้ต่อลูกค้าใหม่โดยไม่ต้องเขียนโค้ดใหม่ทั้งหมด
2. เพิ่ม pipeline view (Kanban) ต่อจากข้อมูลที่เก็บใน Notion/ฐานข้อมูล
3. เพิ่มระบบแจ้งเตือน follow-up อัตโนมัติอย่างง่าย (LINE Notify/อีเมล)

## Checklist

- [ ] มีลูกค้าจริงอย่างน้อย 1 รายขอระบบแบบนี้ก่อนเริ่มทำเวอร์ชัน generalize (เช็คกับ
      [DECISIONS.md](../DECISIONS.md) ADR-0002 ก่อนเริ่ม)
- [ ] Intake bot ตั้งคำถาม/หมวดงานใหม่ได้ผ่าน config ไม่ต้องแก้โค้ดหลัก
- [ ] มี pipeline view แสดง lead ตาม stage
- [ ] มีระบบแจ้งเตือน follow-up อัตโนมัติ
- [ ] ทดสอบกับลูกค้าจริง 1 รายจนใช้งานได้ครบวงจร (รับ lead → ปิดงาน)
- [ ] เขียนเป็น case study ใหม่หลังใช้งานจริงสำเร็จ

## งานที่สามารถรับได้ตอนนี้

ใช้ **Intake Pilot ตัวเดิม** ขายได้ทันทีในชื่อ "AI Intake Bot" — ไม่ต้องรอ generalize เสร็จก่อน
(ดู [08-ai-workflows](../08-ai-workflows/) ที่เป็นมุมขายงานของ skill เดียวกันนี้)

## สิ่งที่ยังไม่ต้องทำ

- ❌ Generalize เป็นโปรดักต์ก่อนมีลูกค้าจริง 1 รายขอ (ตาม ADR-0003/ADR-0002)
- ❌ Email marketing automation, multi-channel (เพิ่ม FB/IG) — เริ่มที่ LINE ก่อนเพราะพิสูจน์แล้วว่าทำงานได้
- ❌ Multi-user / role-based access — ลูกค้า SME ส่วนใหญ่ใน stage นี้มีคนดูแลคนเดียวพอ
- ❌ แปลงเป็น SaaS — รอ [09-saas](../09-saas/) และสัญญาณ demand ตาม ADR-0002
