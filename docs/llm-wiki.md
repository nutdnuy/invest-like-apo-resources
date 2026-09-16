# LLM Wiki for Investors

[← Resources](../README.md)

**[Upstream repository: Migchw/llm-wiki-starter](https://github.com/Migchw/llm-wiki-starter)**

อ่านภาพรวมเพิ่มเติมได้ที่ [DeepWiki overview](https://deepwiki.com/Migchw/llm-wiki-starter/1-overview:-llm-wiki-for-investment-research) ซึ่งเป็นคู่มือประกอบ; รายละเอียดติดตั้งและพฤติกรรมจริงให้ยึดโค้ดและเอกสารใน upstream

โครงการต้นทางเป็น template สำหรับ Obsidian vault และ agent workflow ด้าน investment research ใช้แยกหลักฐานดิบ บันทึกแหล่งข้อมูล ความรู้ที่เชื่อมกัน และร่องรอยการทำงาน

## เตรียมก่อนข้อมูลเข้ามา

- ใช้ขั้นตอนติดตั้งใน README ของ upstream และตรวจ requirements ของเวอร์ชันที่เลือก
- เตรียมโฟลเดอร์ templates, schema, indexes และกติกาของ vault
- กำหนดแหล่งที่อนุญาตให้รับเข้า ข้อมูลวันที่และต้นทางที่ต้องเก็บ และวิธีจัดการหลักฐานที่ขัดกัน
- ทดลองด้วยเอกสารที่เผยแพร่แล้วหนึ่งรายการ และตรวจผล source note เทียบต้นฉบับ

## Ingest เมื่อหลักฐานมาถึง

ข่าว บทความ filing และ transcript ถูก ingest หลังจากมีแหล่งข้อมูลนั้นให้เข้าถึงแล้ว การตั้งระบบล่วงหน้าคือการเตรียมวิธีรับและตรวจข้อมูล

ตัวอย่างคำสั่งของ **โครงการต้นทาง** หลังติดตั้งตาม README:

```text
/ingest <URL>
```

ตรวจรายละเอียดเวอร์ชันล่าสุดที่ [ingest specification](https://github.com/Migchw/llm-wiki-starter/blob/master/.claude/skills/ingest/SKILL.md) คำสั่งนี้ไม่ใช่คำสั่งที่ repository resources นี้ติดตั้งให้

ผลที่ควรตรวจ: ต้นฉบับถูกเก็บไว้, ข้อเท็จจริงแยกจากการตีความ, มีลิงก์กลับแหล่งข้อมูล, มีวันที่เผยแพร่/รับเข้า และมีบันทึกว่าประมวลผลอะไร

## ถ้าต้องการรับข่าวอัตโนมัติ

เตรียมตัวติดตามแหล่งข้อมูลและ scheduler แยกต่างหาก กำหนดรอบตรวจ แหล่งที่อ่านได้ การกันซ้ำ การ retry และแจ้งข้อผิดพลาด การมี ingest queue ไม่ได้แปลว่ามีการตั้งเวลารับข่าวซ้ำให้แล้ว

## ใช้ร่วมกับ workflow นี้

1. ข้อมูลจาก Webull หรือเอกสารต้นทาง → เก็บหลักฐานพร้อม metadata
2. Source note → ให้กรอบวิเคราะห์เลือกข้อมูลที่เกี่ยวข้อง
3. ผลคำนวณและข้อสรุป → อ้างกลับ source note ใน memo และ decision log

คู่มือนี้แนะนำวิธีต่อยอด ไม่ได้อ้างว่าเชื่อม Webull, Python และ Wiki สำเร็จรูปไว้แล้ว
