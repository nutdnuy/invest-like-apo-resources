# Webull: data for investment research

[← Resources](../README.md)

## QuantCorner referral

**[เปิดบัญชี Webull ผ่านลิงก์แนะนำ QuantCorner](https://www.webull.co.th/k/QuantCorner)**

ลิงก์นี้เป็น referral link ของ QuantCorner เงื่อนไขและสิทธิประโยชน์ให้ยึดข้อมูลปัจจุบันบน Webull ไม่ได้หมายความว่าเปิดบัญชีแล้วได้รับสิทธิ์ OpenAPI หรือข้อมูลทุกประเภทโดยอัตโนมัติ

## เริ่มต้น API

1. อ่าน [Individual Application Process](https://developer.webull.co.th/apis/docs/authentication/individual-application/) และขอสิทธิ์ API ตามขั้นตอนของ Webull
2. เมื่ออนุมัติแล้วจึงลงทะเบียน application และสร้าง App Key / App Secret
3. อ่าน [Token](https://developer.webull.co.th/apis/docs/authentication/token/) และ [Signature](https://developer.webull.co.th/apis/docs/authentication/signature/) สำหรับ authentication; ใช้ SDK ที่ตรงกับภูมิภาคและ environment
4. ตรวจสิทธิ์ข้อมูลกับ [Market Data API FAQ](https://developer.webull.co.th/apis/docs/market-data-api/faq/) สิทธิ์ subscription บนแอปกับ OpenAPI แยกจากกัน
5. ทดลอง endpoint สำหรับอ่านข้อมูลก่อน แล้วตรวจ response, หน่วย, วันที่ และข้อจำกัด ก่อนนำไปเข้า Wiki หรือคำนวณ

เก็บ keys ใน environment หรือ secret store ของตนเอง อย่าใส่ keys หรือข้อมูลบัญชีลงใน repository

## ลิงก์ข้อมูลสำหรับเดโม

| แหล่ง | ใช้ดูอะไร |
| --- | --- |
| [API documentation](https://developer.webull.co.th/apis/docs/) | เอกสารรวมและรายการ endpoint ปัจจุบัน |
| [Get Industry Comparison](https://developer.webull.co.th/apis/docs/reference/trade-api/industry-comparison/) | เปรียบเทียบข้อมูลการเงินของหุ้นในอุตสาหกรรมเดียวกัน |
| [Get Analyst Rating](https://developer.webull.co.th/apis/docs/reference/trade-api/get-analyst-rating/) | ข้อมูลจำนวน analyst ratings ตามระดับคำแนะนำ |

Industry Comparison ที่เปิดตรวจเมื่อ 16 September 2026 แสดง endpoint `GET /market-data/fundamentals/industry-comparisons/get` ให้ตรวจ request schema และตลาดที่รองรับจากเอกสารปัจจุบันก่อนเขียนโค้ด ภาพสไลด์เก่าอาจไม่ตรงกับ API เวอร์ชันใหม่

## เก็บอะไรติดมากับข้อมูล

- Provider, endpoint และพารามิเตอร์ที่ใช้ โดยไม่เก็บ authentication headers
- Symbol, ตลาด, สกุลเงิน และหน่วย
- ช่วงงบหรือวันที่ข้อมูลมีผล และเวลาที่ดึงข้อมูล
- รายการที่ขาดหายหรือมีการปรับปรุงย้อนหลัง
- สิทธิ์ในการเก็บและเผยแพร่ต่อของชุดข้อมูล

หน้านี้เป็นทางเข้าคู่มือและแผนเตรียมข้อมูล ไม่มีสคริปต์สั่งซื้อขายหรือการเชื่อมบัญชีที่รันไว้ให้แล้ว
