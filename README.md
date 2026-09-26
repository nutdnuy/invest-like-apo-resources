# Invest like อาโป — Resources

**เครื่องมือ แหล่งอ่าน และแม่แบบสำหรับใช้ AI ช่วยงานวิจัยการลงทุน**

ชุด resources ประกอบการบรรยายของ **QuantCorner** สำหรับ **Claude Thailand Community** ตั้งแต่การรับข้อมูล สะสมหลักฐาน วิเคราะห์ด้วยกรอบที่ใช้ซ้ำ ไปจนถึงแสดงผลและบันทึกการตัดสินใจ

## สไลด์ประกอบการบรรยาย

[ดาวน์โหลดสไลด์ Invest like อาโป (PDF · 31 หน้า)](slides/invest-like-apo-resources-qr.pdf)

## เริ่มจากตรงนี้

1. อ่าน [ภาพรวม workflow](docs/workflow.md) เพื่อเลือกส่วนที่อยากทดลอง
2. เลือกข้อมูลหนึ่งชิ้น เช่น filing หรือ earnings transcript แล้วอ่าน [การตั้ง LLM-Wiki และ ingest](docs/llm-wiki.md)
3. เลือกวิธีวิเคราะห์หนึ่งเรื่องจาก [Book-to-Skill และรายการอ่าน](docs/book-to-skill.md)
4. เก็บหลักฐานด้วย [Source Note](templates/source-note.md) และบันทึกเหตุผลด้วย [Decision Log](templates/decision-log.md)

## Webull × QuantCorner

### [เปิดบัญชี Webull ผ่านลิงก์ QuantCorner](https://www.webull.co.th/k/QuantCorner)

**Referral link:** ลิงก์ด้านบนเป็นลิงก์แนะนำของ QuantCorner โปรดตรวจสอบเงื่อนไขและสิทธิประโยชน์ปัจจุบันกับ Webull การเปิดบัญชีและการขอสิทธิ์ OpenAPI เป็นคนละขั้นตอน

- [คู่มือ Webull สำหรับงานวิจัยในชุดนี้](docs/webull.md)
- [Webull Thailand API documentation](https://developer.webull.co.th/apis/docs/)
- [Get Industry Comparison](https://developer.webull.co.th/apis/docs/reference/trade-api/industry-comparison/)

## เครื่องมือในแต่ละส่วนของงาน

| ส่วนของงาน | Resource | ใช้ทำอะไร |
| --- | --- | --- |
| **Input · Data** | [Webull API](https://developer.webull.co.th/apis/docs/) | ข้อมูลตลาดและข้อมูลพื้นฐานตามสิทธิ์ของบัญชีและ endpoint |
| **Input · Research memory** | [LLM Wiki for Investors](https://github.com/Migchw/llm-wiki-starter) | เก็บต้นฉบับ เชื่อม source notes และสะสมความรู้ที่ย้อนถึงหลักฐานได้ |
| **Process · Reusable methods** | [Book-to-Skill](https://github.com/virgiliojr94/book-to-skill) | เปลี่ยนเอกสารที่มีสิทธิ์ใช้ให้เป็นกรอบ ขั้นตอน และเอกสารอ้างอิงของ agent |
| **Process · Agent skills** | [QuantCorner Agent Skills](https://www.quant-corner.com/agent-skills) | แหล่งรวม Agent Skills ของ QuantCorner |
| **Process · Agent skills** | [Claude Agent Skills](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) | รูปแบบคำสั่งและ resources ที่ agent เรียกใช้ซ้ำเมื่อเกี่ยวข้อง |
| **Process · Portfolio analytics** | [Riskfolio-Lib](https://github.com/dcajasn/Riskfolio-Lib) · [Docs](https://riskfolio-lib.readthedocs.io/en/latest/) | คำนวณ portfolio optimization และความเสี่ยงภายใต้สมมติฐานและข้อจำกัด |
| **Process · Research toolkit** | [AssetManagementToolkit](https://github.com/nutdnuy/AssetManagementToolkit) | วิเคราะห์ผลตอบแทน covariance พอร์ต backtest และ stress test |
| **Output · Dashboard** | [zframes](https://github.com/zentryHQ/zframes) | แสดงข้อมูลผ่าน dashboard และ frames ที่กำหนดไว้ |
| **Output · Decision record** | [Decision Log template](templates/decision-log.md) | เก็บข้อเสนอ หลักฐาน เหตุผล ผู้ทบทวน และเงื่อนไขทบทวนครั้งถัดไป |

การเชื่อมเครื่องมือเป็นแนวทางสำหรับต่อยอด ผู้ใช้ยังต้องกำหนดข้อมูล สิทธิ์เข้าถึง วิธีคำนวณ และตัวเชื่อมข้อมูลของตนเอง

## คู่มือและแม่แบบ

| เอกสาร | เนื้อหา |
| --- | --- |
| [Workflow](docs/workflow.md) | Input → Process → Output และลำดับทดลองทีละส่วน |
| [Webull](docs/webull.md) | Referral, สมัคร API, authentication และเอกสารข้อมูล |
| [LLM-Wiki](docs/llm-wiki.md) | เตรียม vault ก่อน แล้ว ingest เมื่อหลักฐานเข้ามา |
| [Book-to-Skill](docs/book-to-skill.md) | เลือกวิธีวิเคราะห์ แปลง และตรวจวิธีที่ได้ |
| [Reading list](docs/reading-list.md) | หนังสือและหัวข้ออ่านตามบทบาทของงาน |
| [Portfolio & dashboard](docs/portfolio-and-dashboard.md) | Python, Riskfolio-Lib, AssetManagementToolkit และ zframes |
| [Source Note](templates/source-note.md) | ข้อเท็จจริง การตีความ คำถาม และต้นทาง |
| [Analysis Method Worksheet](templates/analysis-method.md) | โครงเตรียมวิธีวิเคราะห์ก่อนพัฒนาเป็น skill |
| [Decision Log](templates/decision-log.md) | บันทึกเหตุผลก่อนรู้ผลลัพธ์ |

## ขอบเขตของชุดนี้

เอกสารนี้ใช้เพื่อการเรียนรู้และจัดกระบวนการวิจัย ไม่ใช่คำแนะนำซื้อขายเฉพาะบุคคล แม่แบบยังต้องปรับและตรวจสอบกับข้อมูลจริงก่อนใช้ตัดสินใจ

ลิงก์พาไปยังเจ้าของโครงการและสำนักพิมพ์โดยตรง สิทธิ์ในซอฟต์แวร์ หนังสือ และเครื่องหมายการค้าเป็นของเจ้าของแต่ละราย ชุดนี้ไม่ได้แจกหนังสือฉบับเต็มหรือคลังข้อมูลบัญชีลงทุน

รวบรวมและตรวจแหล่งอ้างอิง: **16 September 2026** · รายละเอียดติดตั้งและ API ให้ยึดเอกสาร upstream ปัจจุบัน
