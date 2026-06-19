# AI Software Company Blueprint — Career OS ของ zoomib420

Repo นี้คือ **Career OS** — แหล่งความจริงเดียว (single source of truth) ที่พา zoomib420
จากจุดที่ยังไม่มีลูกค้า ไปสู่การรับงาน Web App / Mini CRM / Mini ERP / Automation / AI Workflow / SaaS
และระยะยาวคือการตั้ง **AI Software Company** ของตัวเอง

ไม่ผูกความจำไว้กับ AI ตัวใดตัวหนึ่ง — ChatGPT, Claude, Codex หรือ AI ตัวอื่นในอนาคต
อ่าน repo นี้แล้ว **ต้องสามารถสานงานต่อได้ทันที** โดยไม่ต้องถามย้อนหลังว่า "ตอนนี้อยู่ตรงไหนของแผน"

> 🤖 **ถ้าคุณเป็น AI agent ที่เข้ามาช่วยงานในเซสชันใหม่** ให้อ่าน [AGENTS.md](./AGENTS.md) ก่อนเริ่มทำอะไร
> ไฟล์นั้นมีลำดับการอ่านและกฎการทำงานครบ ไม่ต้องบอกซ้ำทุกครั้งที่เริ่มเซสชันใหม่

---

## เจ้าของ repo

- **ชื่อ:** ปวสิทธิ์ ไชยรัตน์ (Zoom) — GitHub: [zoomib420](https://github.com/zoomib420)
- **ตำแหน่งที่วางไว้:** AI-Powered Builder — รับสร้างเว็บ/แอป/ระบบอัตโนมัติ/AI workflow ให้ทำงานซ้ำๆ กลายเป็นไม่กี่คลิก
- **พื้นฐาน:** จบมนุษยศาสตร์ (ภาษาอังกฤษ), ผ่านงานสอน/ร้านอาหาร/retail & hospitality, มี cert Cybersecurity จาก Future Skills & TryHackMe
- **Portfolio ที่มีอยู่แล้ว:** [creative-portfolio-2026](https://github.com/zoomib420/creative-portfolio-2026) (private) — เว็บ 3D Interactive แบบ "ลิฟต์" พร้อมเคสงานจริง 7 ชิ้น (ดูสรุปวิเคราะห์ใน [02-portfolio/README.md](./02-portfolio/README.md))
- **อีเมลทำงาน:** zoomib420@gmail.com

## เป้าหมาย (เรียงตามลำดับความสำคัญ จริง ไม่ใช่ลอยๆ)

| ลำดับ | เป้าหมาย | สถานะ |
| --- | --- | --- |
| 1 | **First Client + รายได้ก้อนแรก** | 🔴 กำลังทำ ตอนนี้ — ดู [01-first-client](./01-first-client/) |
| 2 | ลูกค้าซ้ำ + เคสงานจริงสะสม (Mini CRM / Mini ERP / Automation / AI Workflow) | ⏳ รอ #1 ก่อน |
| 3 | สร้าง SaaS จากโปรดักต์ที่มีลูกค้าซ้ำพิสูจน์ demand แล้ว | ⏳ รอ #2 ก่อน |
| 4 | AI Software Company (ทีม + agent workflow ของตัวเอง) | ⏳ วิสัยทัศน์ระยะยาว ไม่ใช่งานตอนนี้ |

กฎเหล็กของ repo นี้: **ห้ามข้ามไปทำลำดับถัดไปก่อนลำดับก่อนหน้าจะสำเร็จจริง** (ดูเหตุผลใน [DECISIONS.md](./DECISIONS.md))

## โครงสร้าง repo

```
README.md              ภาพรวมทั้งหมด (ไฟล์นี้)
AGENTS.md               คู่มือสำหรับ AI agent — อ่านลำดับ + กฎการทำงาน (กันการบอกซ้ำทุกเซสชัน)
CURRENT_FOCUS.md        โฟกัสตอนนี้ — อัปเดตทุกครั้งที่เปลี่ยนงาน
ROADMAP.md              แผนระยะสั้น/กลาง/ยาว พร้อม action จริง
PROGRESS.md             สถานะปัจจุบันของแต่ละ stage (snapshot)
CHANGELOG.md            ประวัติการเปลี่ยนแปลงของ repo นี้เอง
DECISIONS.md            บันทึกเหตุผลการตัดสินใจ (ADR-style)

01-first-client/        หาลูกค้าคนแรก + ปิดงานแรก
02-portfolio/           วิเคราะห์/พัฒนา portfolio ให้ขายงาน Business Systems ได้
03-web-app-foundation/  สแต็กเว็บแอปมาตรฐานสำหรับงานลูกค้า
04-database-backend/    ฐานข้อมูล + backend ที่ใช้ซ้ำได้ทุกงาน
05-mini-crm/            โปรดักต์ Mini CRM (ต่อยอดจาก Intake Pilot)
06-mini-erp/            โปรดักต์ Mini ERP (ต่อยอดจาก Schedule Automator)
07-automation/          แพ็กเกจบริการ Automation (ทักษะที่แข็งที่สุดตอนนี้)
08-ai-workflows/        แพ็กเกจบริการ AI Workflow / Chatbot
09-saas/                แปลงโปรดักต์ที่พิสูจน์ demand แล้วเป็น SaaS
10-ai-company/          วิสัยทัศน์ระยะยาว — AI Software Company
templates/              เทมเพลตใช้ซ้ำ (proposal, case study, ADR, ฯลฯ)
```

ทุกโฟลเดอร์ `0X-*` มี README.md ของตัวเองในรูปแบบเดียวกัน: **เป้าหมาย → สิ่งที่ต้องเรียน → โปรเจกต์ที่ต้องทำ →
checklist → งานที่รับได้ตอนนี้ → สิ่งที่ยังไม่ต้องทำ**

## วิธีใช้ repo นี้กับ AI แต่ละตัว

Repo นี้เป็น Markdown ล้วน ไม่ผูกกับ tool เฉพาะ ใช้ได้กับทุก AI ที่อ่านไฟล์ได้ —
รายละเอียดวิธีใช้ต่อ tool และกฎการทำงานของ AI agent ทั้งหมดอยู่ใน [AGENTS.md](./AGENTS.md) ไฟล์เดียว
ไม่ซ้ำซ้อนกับที่นี่

## สถานะตอนนี้

ดูรายละเอียดที่ [PROGRESS.md](./PROGRESS.md) และงานที่ทำอยู่ที่ [CURRENT_FOCUS.md](./CURRENT_FOCUS.md)

เวอร์ชันปัจจุบัน: **v0.1** — วาง Career OS โครงสร้างทั้งหมด ยังไม่มีลูกค้า ยังไม่มีรายได้
