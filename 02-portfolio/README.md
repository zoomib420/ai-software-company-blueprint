# 02 — Portfolio

## เป้าหมาย

ทำให้ [creative-portfolio-2026](https://github.com/zoomib420/creative-portfolio-2026) ใช้ "ปิดงาน" ได้จริง
ไม่ใช่แค่โชว์ฝีมือ creative/3D — ต้องสื่อสารชัดว่า "จ้างคนนี้แล้วธุรกิจฉันได้อะไร" ภายใน 10 วินาทีแรก

## วิเคราะห์สถานะปัจจุบันของ portfolio (อัปเดต 2026-06-19)

### สิ่งที่มีอยู่แล้ว (แข็งมาก ด้านเทคนิค)

- Vite 6 + React 19 + TypeScript strict, React Three Fiber, Tailwind v4, Zustand
- ระบบ Multi-tier Fidelity (WebGPU → WebGL2 → 2D fallback) — โชว์ระดับความสามารถเชิงวิศวกรรมสูง
- Data-driven content (`src/data/profile.ts`, `src/data/projects.ts`) — แก้ไฟล์เดียวอัปเดตทั้งเว็บ
- มี 7 โปรเจกต์อยู่แล้วใน `src/data/projects.ts`: Schedule Automator, Calories Book, Introvert Mind,
  Intake Pilot, Kids Plearn, Z World, ตัวพอร์ตเอง
- เอกสาร AI (`AGENTS.md`, `docs/`) ครบสำหรับให้ AI ช่วยพัฒนาต่อ
- ESLint + GitHub Actions CI, A11y/SEO พื้นฐานพร้อม

### ปัญหาที่กระทบการ "ปิดงานแรก" โดยตรง

1. **ยังไม่ deploy** — ไม่มี URL จริงให้ส่งลูกค้าได้ (`docs/USER_TODO.md` ข้อ 7 ยังไม่ทำ) — นี่คือ blocker
   อันดับ 1 ของ stage 01
2. **ยังเหลือ EXAMPLE placeholder** — SEO/og-image/บางจุดใน `index.html` (ค้นด้วย `git grep -n "EXAMPLE"` ใน
   repo นั้น)
3. **โทนพอร์ตทั้งหมดคือ "Creative Technologist"** — เน้น 3D/เกม/ศิลปะ ไม่มีจุดที่บอกตรงๆ ว่า "รับงาน
   Automation/ERP/CRM ให้ธุรกิจ" ทั้งที่มีเคสจริงรองรับอยู่แล้ว 2 ชิ้น
4. **Schedule Automator และ Intake Pilot ถูกจัดอยู่ใต้ category `automation` เฉยๆ ปนกับเกม/เว็บ** — เคสที่ขายงาน
   B2B ได้ดีที่สุดถูกกลืนไปกับเคสฝั่ง creative/personal project

### ข้อเสนอ: เพิ่ม "Business Systems" ให้ชัดในพอร์ต

ไม่ต้องสร้างเว็บใหม่หรือรื้อโครง 3D ที่ทำไว้แล้ว — เพิ่มแบบ data-driven ตามโครงที่มีอยู่:

- **เพิ่ม category ใหม่ `business-systems`** ใน `src/data/projects.ts` (`projectCategories`) แยกจาก
  `automation` เดิม ให้ Schedule Automator และ Intake Pilot ย้ายมาอยู่ตรงนี้ พร้อม `description` ที่เขียนใหม่
  เป็นกรอบ "ผลลัพธ์ธุรกิจ" (เช่น "ลดเวลาทำตารางจากหลายชั่วโมง/สัปดาห์เหลือไม่กี่คลิก" ไม่ใช่แค่ "ใช้ Selenium")
- **เพิ่ม CTA ชัดในหน้า/section นี้**: "ต้องการระบบแบบนี้ให้ธุรกิจคุณ? [ติดต่อ]" ลิงก์ไปอีเมล/LINE ตรง
- **เพิ่ม `links[]` ที่ชี้ไปเอกสาร case study** (จาก [templates/case-study-template.md](../templates/case-study-template.md))
  แทนที่ `example.com` ที่ยังเป็น placeholder
- ถ้ามีเวลาเหลือหลัง deploy: ทำ **2D one-page fallback แบบเจาะจง B2B** แยกจากเส้นทาง 3D เต็ม สำหรับลูกค้าที่ไม่
  อยากเล่น 3D ลิฟต์ ต้องการแค่อ่านเร็วว่า "ทำอะไรได้บ้าง ราคาเท่าไหร่"

### ที่ที่จะใส่ Mini CRM / Mini ERP / Automation demo ในอนาคต (รอ stage 05–07)

เมื่อสร้าง Mini CRM ([05-mini-crm](../05-mini-crm/)) และ Mini ERP ([06-mini-erp](../06-mini-erp/)) เสร็จเป็น
เดโมที่จับต้องได้แล้ว ให้เพิ่มเป็นโปรเจกต์ใหม่ในหมวด `business-systems` เดียวกันนี้ ไม่ต้องสร้างหมวดเพิ่มอีก —
โครง data-driven ที่มีอยู่รองรับการเพิ่มโปรเจกต์ใหม่ได้โดยไม่ต้องแก้ UI

## สิ่งที่ต้องเรียน

- การเขียน copy ขายผลลัพธ์ธุรกิจ (ดู [templates/case-study-template.md](../templates/case-study-template.md))
- พื้นฐาน deploy บน Vercel (env vars, custom domain, `api/` serverless function ที่มีอยู่แล้วใน repo นั้น)
- SEO พื้นฐานสำหรับหน้าเดียว (title/og/canonical) — ส่วนนี้ทำไว้เกือบหมดแล้ว เหลือแก้ค่าจริง

## โปรเจกต์ที่ต้องทำ

1. Deploy `creative-portfolio-2026` ขึ้น Vercel จริง พร้อม custom domain (ถ้ามี) หรือ subdomain ของ Vercel ก่อนก็ได้
2. แก้ EXAMPLE ที่เหลือทั้งหมด (`git grep -n "EXAMPLE"` ใน repo นั้น)
3. เพิ่ม category `business-systems` + ย้าย Schedule Automator/Intake Pilot เข้ามา + เขียน description ใหม่
4. เพิ่ม CTA ติดต่องานในเซกชันนั้น

## Checklist

- [ ] มี URL จริงที่ใช้ส่งลูกค้าได้
- [ ] ไม่มี `EXAMPLE` เหลือใน repo นั้น (ตรวจด้วย grep)
- [ ] category `business-systems` ถูกเพิ่มและแสดงผลถูกทั้ง 3D และ 2D fallback
- [ ] Schedule Automator และ Intake Pilot มี description แบบกรอบผลลัพธ์ธุรกิจ
- [ ] มี CTA ติดต่อในเซกชัน business systems
- [ ] ลิงก์ `links[]` ของทั้งสองโปรเจกต์ชี้ไปเอกสาร case study จริง ไม่ใช่ `example.com`

## งานที่สามารถรับได้ตอนนี้

ไม่มีโดยตรง — stage นี้คือ "อาวุธ" สำหรับใช้ปิดงานใน [01-first-client](../01-first-client/) ไม่ใช่งานที่ขายเอง

## สิ่งที่ยังไม่ต้องทำ

- ❌ เสียงพากย์ ElevenLabs/Botnoi + QR Code Talk (T-23 ใน repo นั้น)
- ❌ AI Image Remix (T-24)
- ❌ Blockchain certificate verify (T-40)
- ❌ WebGPU shader คุณภาพสูงเพิ่มเติม (T-12 ส่วนขยาย)
- ❌ รื้อโครง 3D/เปลี่ยน concept ลิฟต์ — ของเดิมดีอยู่แล้วด้านเทคนิค ปัญหาคือ "ยังไม่ deploy" ไม่ใช่ "ของไม่ดี"
