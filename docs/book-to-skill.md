# Book-to-Skill: reusable analytical methods

[← Resources](../README.md)

- **Converter:** [virgiliojr94/book-to-skill](https://github.com/virgiliojr94/book-to-skill)
- **QuantCorner Agent Skills:** [quant-corner.com/agent-skills](https://www.quant-corner.com/agent-skills)
- **Skill format:** [Claude Agent Skills documentation](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
- **หนังสือและหัวข้ออ่าน:** [Reading list](reading-list.md)

Book-to-Skill ช่วยจัดเอกสารให้เป็นกรอบวิเคราะห์ decision rules และ references ที่ agent เรียกใช้ตามงาน ผลลัพธ์ต้องตรวจเทียบต้นฉบับและทดลองกับโจทย์จริงก่อนใช้

## เริ่มจากวิธีเดียว

1. เลือกคำถามที่ใช้ซ้ำ เช่น ตรวจคุณภาพกำไร หรือวิเคราะห์ FX exposure
2. ระบุหนังสือ edition และบทที่เกี่ยวข้อง ใช้เฉพาะไฟล์ที่มีสิทธิ์นำมาประมวลผล
3. ติดตั้ง converter ตาม README ต้นทาง ตรวจขั้นตอนและ dependencies ปัจจุบัน
4. ให้ผลที่ต้องการครอบคลุม trigger, required inputs, steps, calculations, checks, output และ chapter references
5. ตรวจทุกสูตรและข้ออ้างกับแหล่งต้นฉบับ แล้วทดลองโจทย์ที่รู้คำตอบเพื่อหาข้อผิดพลาด
6. ระบุ version และข้อจำกัดก่อนนำวิธีนั้นไปใช้ซ้ำ

เริ่มร่างด้วย [Analysis Method Worksheet](../templates/analysis-method.md) ซึ่งเป็นแม่แบบออกแบบวิธี ยังไม่ใช่ skill ที่ติดตั้งและผ่านการประเมินแล้ว

## ตัวอย่างการแมป

| หัวข้อ | วิธีที่อาจเตรียม | สิ่งที่ต้องตรวจ |
| --- | --- | --- |
| Financial statement analysis | ขั้นตอนตรวจ earnings quality และ valuation assumptions | Period, หน่วย, accounting policy และรายการปรับปรุง |
| Quantitative methods | ขั้นตอนสถิติ การทดสอบ และ sensitivity | Data leakage, sample size และความเหมาะสมของสมมติฐาน |
| International finance | วิเคราะห์ FX exposure และ country risk | สกุลเงิน ช่วงเวลา และกรณีเปลี่ยน regime |
| Portfolio construction | ระบุ objective, constraints และ risk budget | Estimation error, ต้นทุน และความไวต่อ inputs |

นี่คือแนวทางพัฒนาวิธี ไม่ใช่การอ้างว่าแปลงหนังสือในรายการอ่านสำเร็จแล้ว ไฟล์ skill ที่ดึงเนื้อหาจากหนังสือยังอยู่ภายใต้สิทธิ์ของต้นฉบับ แม้ converter จะเป็น open source
