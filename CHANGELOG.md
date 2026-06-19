# CHANGELOG.md

บันทึกการเปลี่ยนแปลงของ repo นี้เอง (ไม่ใช่ของโปรเจกต์ลูกค้า) เรียงจากใหม่ไปเก่า
รูปแบบ: `## [เวอร์ชัน] - วันที่` แล้วตามด้วยรายการเปลี่ยนแปลง

## [v0.1] - 2026-06-19

### เพิ่ม
- สร้างโครงสร้าง repo ทั้งหมด: README, CURRENT_FOCUS, ROADMAP, PROGRESS, CHANGELOG, DECISIONS
- สร้างโฟลเดอร์ stage 01–10 พร้อม README.md ของแต่ละ stage (เป้าหมาย/สิ่งที่ต้องเรียน/โปรเจกต์/checklist/งานที่รับได้/สิ่งที่ยังไม่ต้องทำ)
- สร้างโฟลเดอร์ `templates/` พร้อมเทมเพลต client proposal, case study, decision record, weekly progress, client intake brief
- วิเคราะห์ portfolio repo (`creative-portfolio-2026`) และระบุจุดที่ควรเพิ่ม Business Systems / Mini CRM / Mini ERP / Automation case study
- ตั้งโฟกัสแรกของ repo เป็น **First Client** ไม่ใช่ AI Company
- `git init` + push ขึ้น GitHub จริง (origin/main)
- เพิ่ม [AGENTS.md](./AGENTS.md) เป็นจุดเข้าเดียวสำหรับ AI agent (ลำดับการอ่าน + กฎการทำงาน) ย้ายมาจาก
  block ที่เคยอยู่ใน README.md เพื่อไม่ต้องบอก AI ซ้ำทุกเซสชัน

### อัปเดต 2026-06-19 (รอบ 2)
- ยืนยันว่า `creative-portfolio-2026` deploy แล้วจริงที่ https://creative-portfolio-2026.vercel.app/ และไม่มี
  EXAMPLE เหลือใน `index.html` — แก้ [PROGRESS.md](./PROGRESS.md), [CURRENT_FOCUS.md](./CURRENT_FOCUS.md),
  [02-portfolio/README.md](./02-portfolio/README.md) ให้ตรงกับความจริง (blocker เดิมข้อ 1 ปิดแล้ว)
- เขียน case study จริง 2 ชิ้น: [01-first-client/case-study-schedule-automator.md](./01-first-client/case-study-schedule-automator.md)
  และ [01-first-client/case-study-intake-pilot.md](./01-first-client/case-study-intake-pilot.md) — ยังเหลือ
  ช่อง 🟡 ที่ต้องกรอกตัวเลขจริง (ชั่วโมงที่ประหยัดได้ ฯลฯ) เพราะไม่มีข้อมูลยืนยันให้กรอกแทน

### บริบทตอนสร้าง
- ยังไม่มีลูกค้า ยังไม่มีรายได้
- มี portfolio และ 2 เคสงานจริงอยู่แล้ว (Schedule Automator, Intake Pilot) ที่ยังไม่ได้ deploy ขึ้นใช้งานจริง
