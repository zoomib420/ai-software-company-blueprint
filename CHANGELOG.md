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
- เปิดเว็บ `creative-portfolio-2026` จริงผ่านเบราว์เซอร์เพื่อ QA: ไม่มี console error, multi-tier fidelity
  fallback ทำงานถูกต้อง, เนื้อหาตรงกับข้อมูลจริง — พบช่องโหว่เพิ่ม 1 ข้อ: หน้า "ติดต่อ" มีแค่อีเมล/GitHub
  ไม่มี LINE/CTA ชัดเจน บันทึกเป็นงานเปิดใหม่ใน [02-portfolio/README.md](./02-portfolio/README.md)

### อัปเดต 2026-06-19 (รอบ 3)
- ได้ลิงก์ LINE OA จริง (https://lin.ee/w3Fw9o6R) — บันทึก CTA copy พร้อมใช้ใน
  [02-portfolio/README.md](./02-portfolio/README.md) และตัดสินใจใช้ช่องทางเดียวสำหรับทุกหมวดงานไปก่อน (ADR-0007)
- ปรับโครงสร้างราคาเป็นบันได 3 ขั้น (งานแรกจริงๆ/Founding Client/ราคาปกติ) ใน
  [01-first-client/pricing.md](./01-first-client/pricing.md) หลังผู้ใช้รีแอคว่าราคารอบแรกแพงเกินไปสำหรับงานแรก
  (ADR-0008)
- สำรวจ `creative-portfolio-2026` ทั้ง repo เพิ่ม (ไม่ใช่แค่ 2 เคสหลัก) เพิ่มหมวดงาน "รอง" ที่รับได้ใน
  [01-first-client/README.md](./01-first-client/README.md): เว็บแอป/ระบบสมาชิก, quiz funnel, ฟีเจอร์ AI วิเคราะห์
  รูปภาพ — และระบุชัดว่า Roblox game dev กับเว็บ 3D เต็มรูปยังไม่ควรเสนอตอนนี้
- **แก้โค้ดจริงใน `creative-portfolio-2026`:** เพิ่ม LINE (Intake Pilot) เป็น CTA ในหน้า "ติดต่อ" ของพอร์ต
  (`src/data/profile.ts` + `src/components/ui/FloorContent.tsx`) ทดสอบ build/typecheck ผ่านแล้ว push ขึ้น
  GitHub แล้ว (commit `b6567a0`) — Vercel ควร auto-deploy ตาม
- ถอด "ฟีเจอร์ AI วิเคราะห์รูปภาพ" ออกจากหมวดงานที่ขายได้ตอนนี้ เพราะความแม่นยำจริงไม่พอ (ADR-0009)
- เขียน case study เพิ่ม: [01-first-client/case-study-introvert-mind.md](./01-first-client/case-study-introvert-mind.md)
  reframe เป็น quiz funnel สำหรับธุรกิจ — พบข้อมูลไม่ตรงกันใน `projects.ts` (tools เป็น Unity/C# แต่คำอธิบาย
  เป็นเว็บแอป) ต้องให้ผู้ใช้เช็คและแก้ที่ source ก่อนใช้ขายงานจริง
- จัดกลุ่ม "เว็บ 3D เต็มรูป" ใหม่เป็น flagship/credibility piece — เก็บโชว์ในพอร์ตเหมือนเดิม แต่ไม่ตั้งราคาแบบ
  มือใหม่ให้ (ADR-0010) ตามที่ผู้ใช้ทักท้วงว่าไม่ควรจัดรวมกับ "ไม่แนะนำ"
- ยืนยัน CTA LINE ขึ้นจริงบนเว็บที่ deploy แล้ว (เช็คผ่านเบราว์เซอร์อีกรอบ)
- สร้าง [templates/service-agreement-template.md](./templates/service-agreement-template.md) — เอกสารตกลงงาน
  ขั้นต่ำที่ขาดอยู่ ทำได้ทันทีไม่ต้องรอ lead
- **ผู้ใช้ยืนยันว่าไม่มีคนรู้จักที่เข้าเงื่อนไข lead-list เลย** — ค้นเว็บยืนยันว่า Fastwork.co เป็นแพลตฟอร์ม
  ฟรีแลนซ์ไทยที่ SME ใช้จริง มีหมวด chatbot/AI automation ราคาตลาดจริงเริ่มที่ ~฿1,500 (ตรงกับ pricing.md)
  เปลี่ยนกลยุทธ์หา lead จาก warm (ทักคนรู้จัก) เป็น cold/inbound (Fastwork + Facebook groups) เป็นตัวหลัก
  (ADR-0011) แก้ [01-first-client/lead-list.md](./01-first-client/lead-list.md) ตาม

### บริบทตอนสร้าง
- ยังไม่มีลูกค้า ยังไม่มีรายได้
- มี portfolio และ 2 เคสงานจริงอยู่แล้ว (Schedule Automator, Intake Pilot) ที่ยังไม่ได้ deploy ขึ้นใช้งานจริง
