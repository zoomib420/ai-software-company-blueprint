# PROGRESS.md — สถานะปัจจุบันแบบเห็นภาพรวม

> Snapshot ของแต่ละ stage ณ เวลาที่อัปเดตล่าสุด ไม่ใช่ log ประวัติ (ดูประวัติที่ [CHANGELOG.md](./CHANGELOG.md))
> อัปเดตไฟล์นี้ทุกครั้งที่สถานะ stage ไหนเปลี่ยน

**อัปเดตล่าสุด:** 2026-06-19 · **เวอร์ชัน repo:** v0.1

## ภาพรวม

| # | Stage | สถานะ | หมายเหตุ |
| --- | --- | --- | --- |
| 01 | [First Client](./01-first-client/) | 🔴 กำลังทำ — โฟกัสหลักตอนนี้ | ยังไม่มี lead, ยังไม่มี case study พร้อมขาย |
| 02 | [Portfolio](./02-portfolio/) | 🟡 มีพอร์ตอยู่แล้ว แต่ยังไม่ deploy จริง | `creative-portfolio-2026` พร้อม 95% ด้านโค้ด รอ deploy + เติม Business Systems section |
| 03 | [Web App Foundation](./03-web-app-foundation/) | ⚪ ยังไม่เริ่ม | รอ first client ก่อน |
| 04 | [Database & Backend](./04-database-backend/) | ⚪ ยังไม่เริ่ม | รอ first client ก่อน |
| 05 | [Mini CRM](./05-mini-crm/) | ⚪ ยังไม่เริ่ม | มีต้นแบบแนวคิดจาก Intake Pilot แล้ว |
| 06 | [Mini ERP](./06-mini-erp/) | ⚪ ยังไม่เริ่ม | มีต้นแบบแนวคิดจาก Schedule Automator แล้ว |
| 07 | [Automation](./07-automation/) | 🟢 มีฝีมือพร้อมขายแล้ว | ทักษะพิสูจน์แล้วจาก Schedule Automator (ERP reverse-engineering + Sheets sync) |
| 08 | [AI Workflows](./08-ai-workflows/) | 🟢 มีฝีมือพร้อมขายแล้ว | ทักษะพิสูจน์แล้วจาก Intake Pilot (LINE + Notion + AI) |
| 09 | [SaaS](./09-saas/) | ⚪ ยังไม่เริ่ม | รอสัญญาณ demand จากลูกค้าซ้ำ |
| 10 | [AI Company](./10-ai-company/) | ⚪ วิสัยทัศน์ระยะยาว | ไม่ใช่งานตอนนี้ |

สัญลักษณ์: 🔴 กำลังทำ/เร่งด่วน · 🟡 มีความคืบหน้าแต่ยังไม่เสร็จ · 🟢 พร้อมใช้งาน/ขายได้ · ⚪ ยังไม่เริ่ม

## รายได้ & ลูกค้า

| เมตริก | ค่าปัจจุบัน |
| --- | --- |
| จำนวนลูกค้าที่ปิดได้ | 0 |
| รายได้สะสม | ฿0 |
| Lead ที่ติดต่อแล้ว | 0 |
| Case study พร้อมโชว์ | 0 (เป้าหมาย: 2 จาก Schedule Automator + Intake Pilot) |

## Asset ที่มีอยู่แล้วและนำมาใช้ได้ทันที

- **Schedule Automator & Classroom Creator** (2024) — Python/Selenium, ERP→Google Sheet, Google Classroom API → ใช้เป็นเคส [07-automation](./07-automation/) และ [06-mini-erp](./06-mini-erp/)
- **Intake Pilot** (2026) — AI chatbot รับลูกค้า ผูก LINE + Notion API → ใช้เป็นเคส [08-ai-workflows](./08-ai-workflows/) และ [05-mini-crm](./05-mini-crm/)
- **creative-portfolio-2026** — เว็บพอร์ต 3D พร้อมเคสงานจริง 7 ชิ้น (รวม 2 เคสข้างบน) — รอ deploy จริง
- Cert ด้าน Cybersecurity (Future Skills, TryHackMe) — ใช้สร้างความน่าเชื่อถือเรื่อง security เวลาคุยกับลูกค้าองค์กร

## Next checkpoint

ดู next action 7 วันถัดไปที่ [CURRENT_FOCUS.md](./CURRENT_FOCUS.md)
