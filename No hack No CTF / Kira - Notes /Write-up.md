## Tên challenge: Kira - Notes
## Tác giả: UmmIt Kin
## Mảng: Forensics
---
Đầu tiên mình tải file về được 1 tệp sqlite có tên là ```places.sqlite```

<img width="1016" height="428" alt="image" src="https://github.com/user-attachments/assets/c95b28be-506f-4dce-8d7b-598d3db84146" />

mình bỏ file đó vào tool ```SQLite``` để điều tra

<img width="1536" height="863" alt="image" src="https://github.com/user-attachments/assets/8002d273-003d-4a16-a9fa-339349781c96" />

 mình qua Browse Data và bắt đầu tìm kiếm

 <img width="1536" height="863" alt="image" src="https://github.com/user-attachments/assets/3f5341cf-5ee7-447e-9571-b5a895b67665" />

thấy ở table moz_places có nhiều url thú vị như 
```
https://drive.proton.me/urls/00MNVW0SHG#do4wWWpAQ0Lw
```

```
http://151.158.224.74:31337/
```

```
https://github.com/UmmItKin/Kira-Notes
```

Khi phát hiện ra, mình vào ```http://151.158.224.74:31337/``` đầu tiên vì thấy đây khả năng cao là link web của challenge

Mình thấy được giao diện Kira- Notes

<img width="1536" height="863" alt="image" src="https://github.com/user-attachments/assets/9383f110-f767-4c8c-afba-c4c1982a5eb6" />


