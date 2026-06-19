# 08 — AI Workflows

> 🟢 Stage นี้ "พร้อมขายแล้ว" ตั้งแต่ v0.1 — ทักษะพิสูจน์แล้วจาก Intake Pilot ดู [PROGRESS.md](../PROGRESS.md)

## เป้าหมาย

แพ็กเกจทักษะ AI workflow/chatbot ที่มีอยู่แล้ว (AI สัมภาษณ์ลูกค้า, ผูก LINE API + Notion API, ประเมินงาน
อัตโนมัติ) ให้เป็นบริการที่อธิบายและขายให้ลูกค้าใหม่ได้เร็ว

## สิ่งที่ต้องเรียน

- Prompt engineering สำหรับงานธุรกิจจริง (ไม่ใช่แค่ chat ทั่วไป — ต้องดึงข้อมูลที่ใช้ได้ออกมาเป็น structured
  data เช่น budget, ความเร่งด่วน, หมวดงาน)
- พื้นฐาน RAG (Retrieval-Augmented Generation) สำหรับ FAQ bot ที่ตอบจากข้อมูลจริงของธุรกิจลูกค้า ไม่ใช่ตอบจาก
  ความรู้ทั่วไปของโมเดล
- การผูก LLM API (Anthropic/OpenAI) เข้ากับ LINE/เว็บ ผ่าน serverless function อย่างปลอดภัย (กัน key หลุด,
  กัน abuse — pattern เดียวกับที่ทำไว้แล้วใน `api/chat.ts` ของ `creative-portfolio-2026`)
- การวาง guardrail พื้นฐานให้ AI agent ทำงานในธุรกิจจริง (ไม่ตอบเรื่องนอกขอบเขต, มี fallback ให้คนจริงรับช่วงต่อ)

## โปรเจกต์ที่ต้องทำ

1. Generalize Intake Pilot ให้ config คำถาม/หมวดงานต่อธุรกิจใหม่ได้เร็ว (เชื่อมกับงานเดียวกันใน
   [05-mini-crm](../05-mini-crm/))
2. สร้าง RAG FAQ bot demo อย่างง่าย 1 ชุด (ตอบคำถามจากเอกสาร/ข้อมูลธุรกิจที่กำหนด) เพื่อโชว์ลูกค้าใหม่
3. ทำ one-pager แพ็กเกจราคา AI workflow แยกจาก one-pager รวมใน [01-first-client](../01-first-client/)

## Checklist

- [ ] มี one-pager ราคา AI workflow/chatbot
- [ ] เคส Intake Pilot มี case study เวอร์ชันเจาะจง AI workflow (ไม่ใช่เวอร์ชันรวมใน 01-first-client)
- [ ] มี RAG FAQ bot demo ที่โชว์ลูกค้าได้แบบ live
- [ ] มี guardrail พื้นฐาน (ขอบเขตคำตอบ, fallback ไปคนจริง) ในทุก bot ที่ส่งมอบให้ลูกค้า
- [ ] มีวิธีจัดการ API key ที่ปลอดภัย (ไม่ฝังใน client code) เป็นมาตรฐานทุกงาน

## งานที่สามารถรับได้ตอนนี้

- AI chatbot รับลูกค้าหน้าด่าน (LINE/เว็บ) พร้อมประเมิน/คัดกรองอัตโนมัติ
- FAQ bot ตอบคำถามซ้ำๆ จากข้อมูลธุรกิจลูกค้าเอง
- เชื่อม AI workflow เข้ากับเครื่องมือที่ลูกค้าใช้อยู่แล้ว (Notion, Sheets, LINE OA)

## สิ่งที่ยังไม่ต้องทำ

- ❌ Fine-tune โมเดลของตัวเอง — ใช้ API ของ Anthropic/OpenAI ตรงพอสำหรับสเกลตอนนี้
- ❌ Multi-agent orchestration framework ที่ซับซ้อน — Intake Pilot เป็น single-purpose agent ที่ทำงานได้ดีอยู่แล้ว
- ❌ สร้าง LLM gateway/platform ของตัวเอง — รอจนกว่าจำนวนลูกค้า AI workflow มากพอจะคุ้มสร้างโปรดักต์ (ดู
  [09-saas](../09-saas/))
