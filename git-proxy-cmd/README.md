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
