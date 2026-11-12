# Peering Eyes
# Forensics 
# Hard
---
Khi nhận đề là mình nhận được 1 file ram thô và 1 file json của linux, đầu tiên mình xem thử đây là linux version mấy bằng lệnh 

```
python3 ~/volatility3/vol.py -f spooked2.lime banners.Banners
```

và có kết quả là 

<img width="1186" height="378" alt="image" src="https://github.com/user-attachments/assets/4bfbaec4-8bca-44c8-8524-9b48244b92d6" />

nó khớp với thông tin trong file json nên kết luận ta có thẻ dùng vol3 để đọc cấu trúc ram của file lime này 

tiếp theo để tìm tiến trình khả khi ta xài lệnh scan 
```
python3 ~/volatility3/vol.py -f spooked2.lime linux.psaux
```

<img width="1535" height="862" alt="image" src="https://github.com/user-attachments/assets/0f7fccfc-383e-4e3c-86b8-ea80043464f8" />

nhìn vào danh sách tiến trình, ta sẽ thấy ngay một điểm cực kỳ đáng ngờ do user (uid=1000) chạy từ terminal qterminal PID 2311

vì đầy bài có gợi ý là về cam hay web cam gì đó thêm EYEsee.py giống như 1 script của 1 camera nào đó nên ta sẽ khám phá cái tiến trình đó thử 

```
mkdir -p /tmp/vol_out
python3 ~/volatility3/vol.py -o /tmp/vol_out -f spooked2.lime linux.proc.Maps --pid 28906 --dump
```
Sau đó kiểm tra dấu vết EYEsee trong dump vừa trích xuất và đọc ngữ cảnh hằng số flag trong ram 

<img width="917" height="411" alt="image" src="https://github.com/user-attachments/assets/bed78679-bf5a-4d16-a302-e1894adae7ba" />

ta thấy được phần đầu flag, ta thấy có vài mục ảnh gì đó mờ ám nên ta sẽ dùng tà thuật để lục hết ảnh trong file ram đó ra 
```
foremost -t jpg -i spooked2.lime -o out
```
sau đó check mục out 
<img width="492" height="192" alt="image" src="https://github.com/user-attachments/assets/edc38b35-d83e-4665-9fca-b01a2e98bb7a" />

và cd vào jpg

<img width="597" height="132" alt="image" src="https://github.com/user-attachments/assets/aebfd670-1384-4e95-aa7a-078a993a4ec7" />

sau đó xem từng tấm ảnh và tada 

<img width="640" height="480" alt="00214262" src="https://github.com/user-attachments/assets/25ad7021-0585-4993-95c3-c855c5f46a69" />

this flag: ``` spooky{th3y_ar3_w2tch1ng} ```
