# Portfolio analytics and dashboards

[← Resources](../README.md)

## Python calculations

| Tool | แหล่งต้นทาง | บทบาท |
| --- | --- | --- |
| Riskfolio-Lib | [Repository](https://github.com/dcajasn/Riskfolio-Lib) · [Documentation](https://riskfolio-lib.readthedocs.io/en/latest/) | Portfolio optimization, risk contributions และ constraints |
| AssetManagementToolkit | [Repository](https://github.com/nutdnuy/AssetManagementToolkit) | Returns, covariance, portfolio research, simulation, backtests และ stress tests |

เริ่มจากราคาหรือผลตอบแทนที่ตรวจแล้ว ระบุวิธีจัดการข้อมูลขาดหาย ความถี่ หน่วย และช่วงประมาณ จากนั้นกำหนด objective และ constraints ก่อนเลือก solver

เก็บผลคำนวณพร้อมเวอร์ชันโค้ด พารามิเตอร์ ช่วงข้อมูล และ solver status ตรวจว่า weights รวมถูกต้อง อยู่ในข้อจำกัด และผลเปลี่ยนอย่างไรเมื่อเปลี่ยน assumptions

AssetManagementToolkit ระบุใน upstream ว่าเป็นเครื่องมือคำนวณ จำลอง และเสนอผล ไม่เชื่อม broker หรือส่งคำสั่งซื้อขาย

## zframes: presentation layer

**[zentryHQ/zframes](https://github.com/zentryHQ/zframes)** ใช้ agent สร้าง configuration เช่น `dashboard.json` ให้ runtime แสดง dashboard และ frames

การต่อผล Python เข้า dashboard ต้องเตรียม data/provider adapter ให้ตรง schema ของ frame การมีไฟล์กำหนด layout ไม่ได้หมายความว่าคำนวณพอร์ตหรือเชื่อมข้อมูลของเราแล้ว

ตัวอย่างแนวทางต่อข้อมูล:

```text
Validated data
  -> Python calculation + assumptions + run ID
  -> Adapter for the chosen frame/provider schema
  -> zframes dashboard + links to the decision log
```

Live stock-like streams ที่ upstream อธิบายอาจเป็น HIP-3 equity perpetual instruments ควรระบุชนิดสินทรัพย์และแหล่งราคาจริง ไม่ติดป้ายว่าเป็นราคาหุ้น cash market โดยอัตโนมัติ

ใน workflow นี้ใช้ zframes สำหรับแสดงผลและติดตาม การตัดสินใจให้มี [Decision Log](../templates/decision-log.md) ประกอบ
