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

Có rất nhiều thông tin như 
<img width="417" height="77" alt="image" src="https://github.com/user-attachments/assets/ea473d14-a0f2-4a6d-be09-ad42c98919ee" />

<img width="985" height="301" alt="image" src="https://github.com/user-attachments/assets/6e074b2e-e368-4cb8-b977-ba2f818e97d1" />


<img width="928" height="442" alt="image" src="https://github.com/user-attachments/assets/378f5fb1-3912-4c13-8b5a-940637bfe98c" />

<img width="1043" height="607" alt="image" src="https://github.com/user-attachments/assets/2e23fa12-6da2-4a24-abdd-7d5b7f439038" />


Mình đã note lại hết thông tin trên và vào tất cả link có trong web đều bị 404

Tiếp tục mình qua  ``` https://drive.proton.me/urls/00MNVW0SHG#do4wWWpAQ0Lw ```

<img width="1536" height="863" alt="image" src="https://github.com/user-attachments/assets/91783484-2215-4cad-96dc-da89c72870ee" />

Đây mới là mục tiêu chính cần khai thác

Đầu tiên mình xem ảnh <img width="1536" height="863" alt="image" src="https://github.com/user-attachments/assets/84b8d272-cc79-4f1b-98b3-ac28af5c09bc" />

Nhìn giống như pass nhưng bị xé mất một phần

Tiếp theo là ổ đĩa of.img 

và ảnh backup của web Kira-Notes ở link đầu

<img width="1364" height="1197" alt="image" src="https://github.com/user-attachments/assets/f9ca221a-a4d0-48af-b629-194b2eacf92d" />


