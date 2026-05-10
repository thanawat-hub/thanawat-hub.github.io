# Commit Message Convention For My Portfolio
Development Convention (Tailwind CSS)

> **Version:** 1.0  
> **Rule:** Atomic Commit (1 ส่วนย่อย = 1 Commit)  
> **Last Updated:** 2026-05-10

---

## 1. Purpose (วัตถุประสงค์)

เพื่อให้การพัฒนาเว็บไซต์เป็นไปอย่างมืออาชีพและตรวจสอบย้อนกลับได้ง่าย:
- **Efficiency:** กวาดสายตาหาประวัติการแก้ไขได้รวดเร็วผ่านระบบ Tag และ Scope
- **Traceability:** รู้ว่าการเปลี่ยนแปลงกระทบ "ส่วนไหน" ของเว็บไซต์โดยไม่ต้องเปิดดูโค้ด

---

## 2. Commit Message Format

รูปแบบ: `Tag(Scope): Description`

- **Tag:** ประเภทของการเปลี่ยนแปลง (เช่น Created, Added, Fixed)
- **Scope:** พื้นที่หรือโมดูลที่แก้ไข (เช่น nav, hero, about, footer, config)
- **Description:** สรุปสิ่งที่ทำเป็นภาษาไทย (Technical terms ใช้ภาษาอังกฤษได้)

---

## 3. Tags Reference & Root Cause

| Tag | การใช้งาน 
| :--- | :--- |
| **Created** | สร้างไฟล์ใหม่, Component ใหม่ หรือโครงสร้างใหม่ครั้งแรก
| **Added** | เพิ่ม Code ส่วนย่อยเข้าไปในไฟล์เดิม (เช่น เพิ่มปุ่ม, เพิ่ม Link)
| **Edited** | **Refactor** ปรับปรุงคุณภาพ Code โดยที่ UI แสดงผลเหมือนเดิม
| **Fixed** | แก้ไข UI ที่แสดงผลผิด หรือบัคที่เกิดจากความผิดพลาดของเรา
| **Updated** | ปรับปรุง UI/Logic เพราะ **Requirement เปลี่ยน** หรือต้องการเปลี่ยน Content
| **Deleted** | ลบไฟล์หรือ Code ที่ไม่ได้ใช้งานแล้ว
| **Config** | แก้ไขไฟล์ตั้งค่า (เช่น `tailwind.config.js`, `.env`, `package.json`)

### การแยกความแตกต่าง (The Big Three)
- **Edited:** แก้เพื่อให้ Code "สวยขึ้น/อ่านง่ายขึ้น" (คนดูเว็บไม่เห็นความต่าง)
- **Fixed:** แก้เพราะมัน "พังหรือแสดงผลผิด" (คนดูเห็นว่ามันกลับมาทำงานถูกต้อง)
- **Updated:** แก้เพราะเรา "อยากเปลี่ยนเองหรือดีไซน์เปลี่ยน" (คนดูเห็นความเปลี่ยนแปลงใหม่ๆ)

---

## 4. ตัวอย่างการใช้งาน (Examples)

### การสร้างและการเพิ่ม (Creation & Addition)
- `Created(nav): สร้างโครงสร้าง Navbar และ Logo`
- `Added(hero): เพิ่มปุ่มดาวน์โหลด CV ในส่วนหน้าแรก`
- `Added(contact): เพิ่ม Form สำหรับส่งข้อความพร้อม Tailwind Validation`

### การแก้ไขและปรับปรุง (Maintenance)
- `Edited(style): Refactor การใช้สีหลักให้เรียกผ่าน Tailwind Config`
- `Fixed(nav): แก้ไขเมนูภาษาไทยแสดงผลเพี้ยนบน Safari`
- `Updated(about): อัปเดตข้อมูลประวัติการทำงานและทักษะใหม่`
- `Updated(ui): เปลี่ยนโทนสีปุ่มจาก Blue เป็น Indigo ตามดีไซน์ใหม่`

### ระบบและไฟล์ตั้งค่า (System)
- `Config(tailwind): เพิ่ม Custom Screen Size สำหรับหน้าจอ Ultra-wide`
- `Deleted(assets): ลบรูปภาพโปรไฟล์เก่าที่ไม่ได้ใช้งาน`

---

## 5. Development Strategy (Invisible Boxes)

เพื่อให้การเขียน Tailwind CSS เป็นระเบียบ ให้จัดลำดับ Class ดังนี้:
1.  **Layout & Display:** (flex, grid, block, relative, w-, h-)
2.  **Design & Spacing:** (p-, m-, gap-, bg-, text-, border-)
3.  **Responsive & State:** (hover:, md:, lg:)

---