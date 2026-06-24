Tên chall: Vecna's Memory Palace

Mảng: Forensics

Mô tả: After a Hawkins Lab blackout, responders recovered a corrupted memory snapshot. Find the final token to close the incident.

Host: 107.170.70.73:5000

File artifact: https://drive.google.com/file/d/1VywHaKWGQ8g-S4Oviyl52LzQqGaPaGJB/view?usp=sharing

---
Đầu tiên vào host mình thấy được giao diện web

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/22932b0d-0dc6-48dd-afdb-099c71c7ff78" />

sau đó mình tải file artifact về để phân tích được file 

<img width="890" height="357" alt="image" src="https://github.com/user-attachments/assets/1bd75cf9-5ac5-48c1-86cc-0a05fe62a683" />

mình cat thử thì biết được thông tin 

```
=== HAWKINS_LAB_VOLATILE_CAPTURE ===
proc=svchost.exe pid=1948 parent=services.exe
driver=.tmp\mindflayer\resident.sys state=orphaned
radio_tag=UNJX
tv_tag=VAF
clockface=13
DEC0Y_PIPE=Vecna\Clock_One\ringbuffer
noise_0:nInxPHet2cbSHn2yPVL0NCqS
memfrag[4]=UklEPTR8UE9TPTR8U0laRT01M3xCTE9CPTcxNjA3ZDc5N2I2YjdkNzIzMjJmN2U3ZDMxNzA3MTZlMmE2YjYyNzEzZDJmM2IyNDJhMjUw
cache_shadow[0]=UklEPTh8UE9TPTR8U0laRT0xMnxCTE9CPWRlYWRjYWZlYmFiZQ==
noise_1:U054PXwLexPCKEBhiR7xLzJy
memfrag[1]=UklEPTF8UE9TPTN8U0laRT01M3xCTE9CPTY2OTczNmM2NDJlNzgzNDc5MmIyZjY3MmQ3OTZmMmQ3MTdjNjQyYzc3NjY3ZDc5N2E2Njdk
cache_shadow[1]=UklEPTJ8UE9TPTl8U0laRT0xMHxCTE9CPTQxNDE0MTQxNDE=
noise_2:oiYVPQ5rAO3V7GS2Vqy9h1Wl
memfrag[5]=UklEPTV8UE9TPTJ8U0laRT01M3xCTE9CPTNhM2EzMjNhMjIzODNlM2IzYTBjMjYyODMwMjMzZDNkM2IyMTI3MjM2OTY1NmMyMDIwMjA2
noise_3:cc8fSspC/O0rb1rOzSkfa56K
memfrag[0]=UklEPTB8UE9TPTF8U0laRT01M3xCTE9CPWIyMTE3MmQzODJhMmQyYjIxNjYyNTNiMjc2YjYyNzEyYjIwM2EzYjI4MjczNDI2NjM2ZDY5
noise_4:G/BuWOA3uS9HoKXY12jIk5US
memfrag[2]=UklEPTJ8UE9TPTV8U0laRT01M3xCTE9CPWMzYzJlM2MyZTI3NmM2OTZhMTIxNDA0MDYxZTAwNjUwMDFmMDQxMDYzNjI3MTc5NjI2OTM0
noise_5:bQbZGWckADMyJzMrxwhQ9NNp
memfrag[3]=UklEPTN8UE9TPTB8U0laRT01M3xCTE9CPTMzNjMzNjM5M2QyNzM1MjkyMjIzMTQyNzJmM2UyZDYzNmQ2OTI0MjczZDJjMjczYjJhMzAy
diag=heap snapshot complete
analyst_note=fragment metadata survived even when the slab order did not
=== END_CAPTURE ===
```
Nhìn sơ qua thấy khá nhiều dữ liệu nhiễu như noise_1, cache_shadow nhưng có vài trường đáng chú ý:
```
radio_tag=UNJX
tv_tag=VAF
clockface=13
```
Ngoài ra còn có:
```
analyst_note=fragment metadata survived even when the slab order did not
```
Dòng note này cho biết dữ liệu đã bị xáo trộn thứ tự, nhưng metadata vẫn còn nguyên

=> Khả năng cao phải dựa vào metadata để ghép lại các fragment

