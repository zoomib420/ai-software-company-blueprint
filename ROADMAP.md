# ROADMAP.md — แผนระยะสั้น / กลาง / ยาว

สถานะ: `[ ]` ยังไม่เริ่ม · `[~]` กำลังทำ · `[x]` เสร็จ
กฎ: ทุก item ต้องเป็น action ที่ทำได้จริง ห้ามเป็นคำกว้างๆ ลอยๆ
รายละเอียดแต่ละ stage อยู่ใน README.md ของโฟลเดอร์ `0X-*`

---

## ระยะสั้น (0–30 วัน) — โฟกัส: First Client

อ้างอิงเต็มที่ [01-first-client/README.md](./01-first-client/) และ [CURRENT_FOCUS.md](./CURRENT_FOCUS.md)

- [ ] Deploy `creative-portfolio-2026` ขึ้น Vercel ให้มี URL ใช้งานจริง
- [ ] แก้ EXAMPLE/placeholder ที่เหลือใน portfolio (SEO, og-image, ลิงก์ social จริง)
- [ ] เพิ่มเซกชัน/โฟลเดอร์ "Business Systems" ในพอร์ตที่ดึง Schedule Automator + Intake Pilot มาเป็นเคสนำ
- [ ] เขียน case study 1 หน้า (PDF/markdown) อย่างน้อย 2 ชิ้น จาก [templates/case-study-template.md](./templates/case-study-template.md)
- [ ] กำหนด service offer ที่ขายได้ทันที 1–2 ชนิด + ราคาเริ่มต้น (ดูตัวเลือกใน 01-first-client)
- [ ] สร้างลิสต์ lead 20 รายที่มีงานซ้ำมือ (กวดวิชา/ร้านค้า/คลินิก/เอเจนซี่ขนาดเล็ก)
- [ ] ส่ง outreach ≥5 ราย/สัปดาห์ โดยใช้ [templates/client-proposal-template.md](./templates/client-proposal-template.md)
- [ ] ปิด **first client** อย่างน้อย 1 ราย (เป้าหมายแนะนำ: ภายใน 2026-08-15 — ปรับได้ตามจริง)
- [ ] รับเงินก้อนแรกเข้าบัญชี → บันทึกใน [PROGRESS.md](./PROGRESS.md) และ [CHANGELOG.md](./CHANGELOG.md)

## ระยะกลาง (1–6 เดือน) — โฟกัส: ทำซ้ำงานที่ขายได้ + เริ่มทำ Mini CRM / Mini ERP / Automation จริง

อ้างอิงเต็มที่ [05-mini-crm](./05-mini-crm/), [06-mini-erp](./06-mini-erp/), [07-automation](./07-automation/), [08-ai-workflows](./08-ai-workflows/)

- [ ] วางสแต็กเว็บแอปมาตรฐานสำหรับงานลูกค้า (ดู [03-web-app-foundation](./03-web-app-foundation/))
- [ ] วาง backend/DB ที่ใช้ซ้ำได้ทุกงาน (ดู [04-database-backend](./04-database-backend/))
- [ ] สร้าง "Mini CRM" จากการต่อยอด Intake Pilot ให้กลายเป็นเทมเพลตขายซ้ำได้
- [ ] สร้าง "Mini ERP" จากการต่อยอด Schedule Automator ให้กลายเป็นเทมเพลตขายซ้ำได้
- [ ] สร้างเทมเพลต Automation อย่างน้อย 2–3 แบบที่ demo ให้ลูกค้าใหม่ได้เร็ว (Sheet↔Notion, Form→LINE→Sheet)
- [ ] ปิดลูกค้าเพิ่มอีกอย่างน้อย 3 ราย รวมเป็น 4 รายขึ้นไป
- [ ] เก็บ case study จากลูกค้าจริงทุกราย (ไม่ใช่เคสสมมติ)
- [ ] เริ่ม upsell/retainer ให้ลูกค้าเดิม (ดูแลรายเดือน) เพื่อสร้างรายได้ประจำ

## ระยะยาว (6–18+ เดือน) — โฟกัส: SaaS → AI Software Company

อ้างอิงเต็มที่ [09-saas](./09-saas/), [10-ai-company](./10-ai-company/)

- [ ] เลือก 1 โปรดักต์ (Mini CRM หรือ Mini ERP) ที่มีลูกค้า ≥3 รายขอ feature คล้ายกันซ้ำ → เป็นสัญญาณ demand จริง
- [ ] แปลงโปรดักต์นั้นเป็น SaaS (multi-tenant, auth, billing ผ่าน Stripe/Omise)
- [ ] เริ่ม outsource/จ้างงานที่ทำซ้ำได้ (เช่น automation script เบื้องต้น) เพื่อขยาย throughput
- [ ] วาง service catalog + agent workflow ภายในของตัวเอง (ใช้ AI agent ช่วยทำงานหลายโปรเจกต์พร้อมกัน)
- [ ] จดทะเบียนธุรกิจ/ตั้งทีมจริงเมื่อรายได้ยืนยัน demand เพียงพอ → กลายเป็น AI Software Company

## กฎการใช้ ROADMAP นี้

1. ห้ามเริ่มงานในระยะกลางก่อนระยะสั้นข้อ "ปิด first client" จะติ๊กเสร็จ
2. ห้ามเริ่มงานในระยะยาวก่อนมีลูกค้าซ้ำที่พิสูจน์ demand จริงในระยะกลาง
3. ถ้าจะข้ามกฎข้อ 1–2 ด้วยเหตุผลเฉพาะหน้า ต้องบันทึกเหตุผลใน [DECISIONS.md](./DECISIONS.md) ก่อนทำ
