# 07 — Automation

> 🟢 Stage นี้ "พร้อมขายแล้ว" ตั้งแต่ v0.1 — ทักษะพิสูจน์แล้วจาก Schedule Automator ดู
> [PROGRESS.md](../PROGRESS.md)

## เป้าหมาย

แพ็กเกจทักษะ automation ที่มีอยู่แล้ว (Selenium, reverse engineering ระบบไม่มี API, sync ข้าม platform) ให้
เป็นบริการที่อธิบายและขายให้ลูกค้าใหม่ได้เร็ว ไม่ต้องอธิบายใหม่ทุกครั้งที่คุยกับ lead

## สิ่งที่ต้องเรียน

- เครื่องมือ no-code/low-code เสริม (n8n, Make) สำหรับงานที่ไม่จำเป็นต้องเขียน Selenium script เอง — ลดเวลา
  ส่งมอบสำหรับงานเล็กๆ
- พื้นฐาน RPA (Robotic Process Automation) ในระดับแนวคิด เพื่อรู้ว่าเมื่อไหร่ควรใช้ Selenium เมื่อไหร่ควรใช้
  no-code
- API integration pattern ทั่วไป (webhook, polling, OAuth พื้นฐาน) สำหรับเชื่อมระบบที่มี API จริง

## โปรเจกต์ที่ต้องทำ

1. สร้างเทมเพลต automation 2–3 แบบที่ demo ให้ลูกค้าใหม่ได้เร็ว:
   - Google Sheet ↔ Notion sync สองทาง
   - Form (เว็บ/Google Form) → แจ้งเตือน LINE → log ลง Sheet
   - ระบบดึงข้อมูลจากเว็บ/ระบบเดิมที่ไม่มี API (ต่อยอด pattern จาก Schedule Automator)
2. ทำ one-pager แพ็กเกจราคา automation แยกจาก one-pager รวมใน [01-first-client](../01-first-client/)
   เผื่อต้องส่งเฉพาะหมวดนี้ให้ lead ที่สนใจ automation อย่างเดียว

## Checklist

- [ ] มีเทมเพลต automation อย่างน้อย 2 แบบ พร้อม demo ให้ลูกค้าดูได้ภายในนัดเดียว
- [ ] มี one-pager ราคา automation
- [ ] เคส Schedule Automator มี case study เวอร์ชันเจาะจง automation (ไม่ใช่เวอร์ชันรวมใน 01-first-client)
- [ ] รู้ตัดสินใจได้ว่างานไหนใช้ no-code (เร็ว) งานไหนต้องเขียนสคริปต์เอง (ระบบไม่มี API/ซับซ้อน)

## งานที่สามารถรับได้ตอนนี้

- Sync ข้อมูลระหว่าง Sheet/Notion/ระบบที่มี API
- ดึงข้อมูลจากระบบเดิมที่ไม่มี API (เก่งด้านนี้อยู่แล้วจาก Schedule Automator)
- แจ้งเตือนอัตโนมัติข้ามแพลตฟอร์ม (เว็บ/ฟอร์ม → LINE/อีเมล)
- งานลดงานมือซ้ำๆ ทั่วไปที่ลูกค้าทำ manual อยู่ทุกวัน/ทุกสัปดาห์

## สิ่งที่ยังไม่ต้องทำ

- ❌ ลงทุนเรียนเครื่องมือ RPA ระดับ enterprise (เช่น UiPath) — เกินความจำเป็นสำหรับลูกค้าขนาดที่กำลังเข้าถึงตอนนี้
- ❌ สร้างแพลตฟอร์ม automation ของตัวเอง — ใช้เครื่องมือที่มีอยู่ (n8n/Selenium/API ตรง) ก่อน จนกว่าจะเห็น
  pattern ซ้ำมากพอที่จะคุ้มสร้างโปรดักต์ (ดู [09-saas](../09-saas/))
