# [How to] วิธีการตั้งค่า Git บน Windows ให้ใช้งานผ่าน Proxy

![alt Git-Logo-2Color](https://raw.githubusercontent.com/adison-meesin/md-file/main/git-proxy-cmd/Git-Logo-2Color.webp)

# List of contents

ผมเขียนอธิบายอย่างละเอียดไว้ในบทความนี้แล้ว  

- [Global config](/blog/what-is-apache-maven/)
- [Local config](/blog/what-is-apache-maven/)
- [Config proxy server](/blog/what-is-apache-maven/)
- [Config authenticate proxy server](/blog/what-is-apache-maven/)
- [View proxy config](/blog/what-is-apache-maven/)
- [Remove proxy config](/blog/what-is-apache-maven/)

# View proxy config

สำหรับการดูค่า Proxy ที่กำหนดไปแล้ว สามารถดูได้ด้วยคำสั่ง ดังนี้


- สำหรับ HTTP Proxy

```sh
$ git config --global http.proxy
```

- สำหรับ HTTPS Proxy

```sh
$ git config --global https.proxy
```


# Clean code คืออะไร

Clean code คือ code สะอาดครับ คำว่าสะสาดอาจจะหมายถึง อ่านง่าย แก้ไขง่าย ต่อยอดง่าย แต่เราจะทำยังไงให้มันได้อย่างที่เราบอกกันละ ก่อนอื่นเราต้องรู้จัก Bad code กันก่อน

# Bad code

เราอาจจะเคยต้องอ่านโค๊ทต่อจากคนอื่น หรือ เราไม่ได้ทำ Project นั้นนานๆ แล้วกลับมาอ่านสิ่งที่เราจะเจอ

- ตัวแปลตัวนี้คืออะไรวะ dowData อ่านชื่อแล้วงง
- function นี้มันทำอะไรวะ genAcTcUserSta
- อ่าน code แล้วต้องลงไปดูใน function เพราะชื่อไม่สื๋อ
- เรา check if เพื่ออะไรวะ for ตรงนี้ไม่เห็นจำเป็นต้องมีนิ
- บางตัวแปลไม่ได้ใช้ประกาศทำไม
- ฯลฯ

สิ่งเหล่านี้ที่เราเจอมาล้วนเป็นหนี้สินทาง software ทั้งสิ้น

# หนี้สินทาง software คืออะไร

มันคือสิ่งที่ทำให้เราช้าลง เพราะหนี้สินล้วนมีดอกเบี้ย สิ่งที่จะเกิดผลกระทบ

- เวลาในการศึกษา code นั้นๆ จะมากขึ้น เช่น มีคนใหม่เข้าทีมอ่านทีหัวแตก (learning curve สูง)
- การแก้ไขโปรแกรมทำได้ยาก ไม่ว่าจะเพิ่ม feature หรือ fix bug
- เขียน test ยาก (ถึงกับไม่รู้จะเขียนยังไง)
- อ่านยากมากๆ อ่าน code แล้วอยากลาออก
- ฯลฯ

วันหนึ่งจะมีคนพูดว่า "ถ้าอ่านยากขนาดนี้ เขียนใหม่ยังง่ายกว่า"

# แนวคิดเรื่อง Clean code

ถ้าเราถามว่า code ทำงานได้ กับ code สวย อะไรสำคัญกว่ากัน
หลายคนคงตอบไม่ยากว่า งานเสร็จ code ทำงานได้สำคัญกว่าอยู่แล้ว
ความเร็วในการออกของสำคัญมากยิ่งเราอยู่ในโลกของ agile และ scrum

ผมก็จะบอกว่าถูกครับ

เรามองว่า Clean code เป็นสิ่งเล็กๆ แต่คุณลองคิดถึงเวลาคุณมีบ้าน ที่ประตูปิดไม่สนิท เวลาปิดมีเสียง เอี๊ยดดดๆ เหมือนในหนังผี กระเบื้องห้องน้ำเรียงมั่ว ก๊อกน้ำน้ำรั่ว
บางปลั๊กไม่มีไฟ ถามว่าเป็นบ้านไหม เป็น อยู่ได้ไหม ก็อยู่ได้ แต่ทุกสิ่งที่กล่าวมาล้วนปัดเป่าเสน่ของบ้านทั้งสิ้น

จงให้ความสำคัญกับสิ่งเล็กๆ ในสิ่งเล็กๆ ล้วนสำคัญ
คนธรรมดากับมืออาชีพ ต่างกันที่ความใส่ใจในรายระเอียด

แต่เรามักถูกบีบด้วยเวลา และคนเดินมาเร่งมากมาย เวลาเกิดปัญหาเราก็จะบอกว่า

- ผมมีเวลาแค่นี้ครับ
- ได้แค่นี้ก็หรูแล้ว
- มันทำงานได้ก็โอเคร

จริงๆ แล้วไม่ใช่แค่ Programmer ที่จะต้องเข้าใจในคำว่า หนี้สินทาง software ขอเรียก software debt คำนี้มันเกิดตอนที่ ลุง Robert C. Martin อธิบายให้หัวหน้าฟังเพราะบริษัทที่ทำงานนั้นเกี่ยวกับด้านการเงินเลยเกิดคำนี้มาเพื่อให้หัวหน้าเข้าใจ มันแปลว่าหัวหน้า , PM ใครก็แล้วแต่ที่สั่งเรา ต้องเข้าใจ
ในเรื่อง software debt ด้วยเพื่อใช้ในการประเมิณเวลาในการทำด้วย

# หลักการในการ Clean Code

# Meaningful Names

การตั้งชื่อ

# Use Intention-Revealing Names

ชื่อทุกสิ่งที่เราตั้งล้วนต้องมีความหมาย บ่งบอกถึงเจตนาของสิ่งนั้นๆ อย่างชัดเจน เช่น class function val หากชื่อพวกนั้นต้องการ comment แสดงว่าชื่อนั้นยังไม่บอกเจตนาอย่างชัดเจน

# Use Pronounceable Names

ชื่อต้องอ่านออกเสียงได้ หลีกเลี่ยงการใช้