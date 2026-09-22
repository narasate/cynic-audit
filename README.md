# Cynic Audit (Universal Edition - V.1) 🔍

> **ทักษะและมาตรฐานการตรวจสอบโค้ดและระบบสากลแบบจับข้อบกพร่องโดยอิงเหตุผลและหลักฐาน (Universal Critical & Skeptical Audit)**
> ใช้ตรวจสอบโปรแกรมได้ทุกประเภท (Web, Mobile, Backend API, Desktop, CLI, Data Pipeline)

---

## 🎯 ปรัชญาการตรวจ (Presumption of Failure)

Cynic Audit ยึดหลัก **"การตั้งสมมติฐานว่าโค้ดมีข้อผิดพลาดไว้ก่อน"**:
1. **Never Trust Inputs**: ข้อมูลนำเข้าอาจผิดรูปแบบ ว่างเปล่า หรือแฝงอักขระพิเศษเสมอ จนกว่าจะมี Validation
2. **Never Assume Success**: การเรียกฟังก์ชัน เครือข่าย หรือฐานข้อมูลอาจล้มเหลวเสมอ จนกว่าจะมี Error Handling
3. **Never Assume Intuitive Interface**: ส่วนต่อประสานอาจทำให้ผู้ใช้สับสน ใช้งานผิดพลาด หรือเข้าใจสถานะผิดเสมอ
4. **Zero Flattery (ไม่มีคำชม 100%)**: รายงานเฉพาะข้อเท็จจริง ปัญหา และผลกระทบเชิงเทคนิค

---

## 🚀 วิธีการติดตั้งและใช้งาน

### 1. ใช้งานใน Claude Code (Anthropic CLI)
คัดลอกไฟล์คำสั่งไปไว้ในโฟลเดอร์คำสั่งของ Claude Code:
* **เฉพาะโปรเจกต์**: `.claude/commands/cynic-audit.md`
* **ทุกโปรเจกต์ในเครื่อง (Global)**: `~/.claude/commands/cynic-audit.md`

**การเรียกใช้งานใน Claude Code:**
```bash
/cynic-audit js/app.js
```
หรือหากต้องการตรวจโปรเจกต์:
```bash
/cynic-audit
```

---

### 2. ใช้งานใน Google Antigravity
คัดลอกโฟลเดอร์สกิลไปไว้ใน Customization Root:
* **ระดับ Workspace**: `.agents/skills/cynic-audit/SKILL.md`
* **ระดับ Global**: `~/.gemini/config/skills/cynic-audit/SKILL.md`

เรียกใช้งานโดยพิมพ์สั่ง Agent:
```
ใช้ cynic-audit ตรวจสอบไฟล์ js/app.js
```

---

## 📋 ขั้นตอนการทำงาน 7 ขั้นตอน (Workflow)

```
[1. สแกนหาโดเมน & ขอบเขต] ➔ [2. สกัดสมมติฐาน] ➔ [3. ตรวจ 3 ระดับมาตรฐาน] ➔ [4. ตรวจ UX/UI/CLI] ➔ [5. ตรวจเจาะลึก 1-3 จุดเสี่ยง] ➔ [6. จำลองสถานการณ์ & ประเมินความรุนแรง] ➔ [7. รายงานผลพร้อมทางแก้และวิธีตรวจ]
```

### 3 ระดับมาตรฐาน:
* **ระดับที่ 1**: ตรรกะฟังก์ชัน, การคำนวณ, Silent Failures (`catch` ว่าง), Secrets & Magic Values, Loop & Resource Safety, Event Listener Leaks
* **ระดับที่ 2**: Data Flow, State Integrity, Contract Mismatch ข้ามโมดูล, Cache Desynchronization, Sensitive Data Exposure, Network Timeout & Fallback, AI & Prompt Safety
* **ระดับที่ 3**: Domain Reality (สอดคล้องกับมาตรฐานทางธุรกิจและกฎหมาย), Export/Print Reality

---

## 📄 รูปแบบรายงานผล

ดูเทมเพลตตัวอย่างฉบับเต็มได้ที่ [templates/report-template.md](templates/report-template.md)

---

## 📜 License
MIT License - Copyright (c) 2026 Narasate
