## Tên challenge: EX-BOOST
## Tác giả: blunderous_wonders
## Mảng: Forensics
---
 Đầu tiên mình tải 3 ảnh về máy 

 <img width="732" height="326" alt="image" src="https://github.com/user-attachments/assets/ecdf4a75-52f3-43d6-aacf-5a49240ed7ea" />

Mô tả chall cũng đã gợi ý về màu rgb và nhắc mình chú ý về các thanh năng lượng, nên mình  quyết định quăng 3 file ảnh lên zsteg để phân tích các lớp màu ra để phân tích: 

 ở ảnh Tiger.png 

 <img width="164" height="146" alt="image" src="https://github.com/user-attachments/assets/ff3f59d2-9009-42d8-b2fc-450c9b971803" />

trong kênh red có chữ ẩn là F33L

<img width="865" height="380" alt="image" src="https://github.com/user-attachments/assets/5f77c16f-a3aa-4813-8856-f9f3ef306872" />


ở ảnh snake.png 

<img width="111" height="96" alt="image" src="https://github.com/user-attachments/assets/72fdee6a-e820-4de4-aef1-726778804855" />

trong kênh green có kí tự ẩn là TH3

<img width="717" height="366" alt="image" src="https://github.com/user-attachments/assets/73a62a47-7912-46ff-83cb-3c9693f9c083" />


ở ảnh Crane.png 

<img width="154" height="136" alt="image" src="https://github.com/user-attachments/assets/b6657fa7-374b-4b1a-b5ba-19ef03e3123e" />

trong kênh blue có kí ẩn là H34T

<img width="965" height="516" alt="image" src="https://github.com/user-attachments/assets/6065f357-2223-4228-bfb3-6bf196c43352" />

và ghép 3 chữ lại dù theo thứ tự RBG hay theo mô tả là các thanh năng lượng thì cũng đều được F33LTH3H34T

## flag là bronco{F33LTH3H34T}
