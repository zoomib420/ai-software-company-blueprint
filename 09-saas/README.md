# 09 — SaaS

> ⚪ ยังไม่เริ่ม — รอสัญญาณ demand ตาม [DECISIONS.md](../DECISIONS.md) ADR-0002 ก่อนแตะ stage นี้

## เป้าหมาย

แปลงโปรดักต์ที่พิสูจน์ demand จริงแล้ว (จาก [05-mini-crm](../05-mini-crm/) หรือ
[06-mini-erp](../06-mini-erp/)) เป็น SaaS ที่ขายเป็น subscription ให้ลูกค้าหลายรายพร้อมกัน แทนการขายเป็นงาน
custom ทีละราย

**เงื่อนไขก่อนเริ่ม stage นี้จริงจัง:** มีลูกค้า ≥3 รายขอ feature คล้ายกันซ้ำในโปรดักต์เดียวกัน (สัญญาณว่า
demand เป็นแบบทั่วไป ไม่ใช่ความต้องการเฉพาะเจ้าใดเจ้าหนึ่ง)

## สิ่งที่ต้องเรียน

- Multi-tenancy pattern (แยกข้อมูลลูกค้าแต่ละรายให้ปลอดภัยในฐานข้อมูลเดียว หรือแยก schema/database ต่อ tenant)
- Billing/subscription (Stripe หรือ Omise สำหรับตลาดไทย) — trial, upgrade/downgrade, invoice
- Onboarding flow ที่ลูกค้าใหม่ self-service ได้บางส่วนโดยไม่ต้องให้เราตั้งค่าให้ทุกครั้ง
- Pricing model สำหรับ SaaS (ต่างจาก one-off project pricing ที่ใช้ใน stage ก่อนหน้า)
- พื้นฐาน customer support/SLA เมื่อมีลูกค้าหลายรายพร้อมกัน

## โปรเจกต์ที่ต้องทำ

1. เลือกโปรดักต์ 1 ตัว (Mini CRM หรือ Mini ERP) ที่มีสัญญาณ demand ชัดที่สุด
2. ออกแบบ multi-tenant data model ต่อจาก [04-database-backend](../04-database-backend/)
3. ผูก billing (Stripe/Omise) เข้ากับ subscription plan
4. ทำ onboarding flow self-service เบื้องต้น

## Checklist

- [ ] มีลูกค้า ≥3 รายขอ feature คล้ายกันซ้ำ (บันทึกหลักฐานไว้ใน [PROGRESS.md](../PROGRESS.md))
- [ ] เลือกโปรดักต์ที่จะทำ SaaS แล้วบันทึกเหตุผลใน [DECISIONS.md](../DECISIONS.md)
- [ ] มี multi-tenant data model
- [ ] มี billing/subscription ทำงานจริง (รับเงินอัตโนมัติได้)
- [ ] มี onboarding flow ที่ลูกค้าใหม่ self-service บางส่วนได้
- [ ] ลูกค้าเดิม (จาก one-off project) ย้ายมาใช้เวอร์ชัน SaaS ได้อย่างน้อย 1 ราย

## งานที่สามารถรับได้ตอนนี้

ไม่มี — stage นี้คือการสร้างโปรดักต์ของตัวเอง ไม่ใช่งานรับจ้าง รอจนกว่าเงื่อนไข demand ข้างบนจะครบก่อน

## สิ่งที่ยังไม่ต้องทำ

- ❌ เริ่มออกแบบ SaaS ก่อนมีสัญญาณ demand ตามเงื่อนไขข้างบน (ผิด ADR-0002 โดยตรง)
- ❌ ทำ SaaS หลายโปรดักต์พร้อมกัน — เลือกตัวที่ demand แรงที่สุดตัวเดียวก่อน
- ❌ ระดมทุน/หา investor — ยังเร็วเกินไป พิสูจน์ recurring revenue ด้วยลูกค้าจริงก่อน
