# WebSocket คืออะไร ทำงานยังไง (อธิบายแบบละเอียด)

# WebSocket

- เป็น `Protocol` ตัวนึง ***** (ขอย้ำว่ามันคือ Protocol) 
- ทำงานอยู่บน Socket ที่เป็น Connection แบบ TCP (Transmission Control Protocol) 
- รองรับ Full Duplex หรือ Bidirectional Communication (การสื่อสารแบบสองทิศทาง หมายถึง เป็นผู้รับและผู้ส่งได้ในเวลาเดียวกัน)
- เป็นมาตรฐานที่ถูกกำหนดโดย IETF (Internet Engineering Task Force) รหัส [RFC6455 (The WebSocket Protocol)](https://tools.ietf.org/html/rfc6455) 
- สร้างขึ้นในปี 2011 (ประมาณ 10 ปีที่แล้ว ณ ตอนที่เขียนบทความนี้)
- นิยมนำมาใช้กับระบบที่ต้องการการอัพเดทข้อมูลแบบ Realtime เช่น ระบบ Chat, ระบบ Notification, ระบบหุ้น, Game, Developer Tools และอื่น ๆ
