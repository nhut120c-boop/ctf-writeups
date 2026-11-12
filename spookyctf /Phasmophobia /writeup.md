## Phasmophobia
**tác giả: Nexus Nova**
**mảng: forensics**
---
Đây là 1 bài khá cơ bản, mình nghĩ lí do nó được điểm cao là do tác giả không nói rõ cách để liên kết 2 flag lại và cách biểu diễn flag còn khá khó nhìn

Đầu tiên mình xài Audacity để phân tích tệp wav là dễ dàng thấy được nội dung 

<img width="1153" height="490" alt="image" src="https://github.com/user-attachments/assets/eaadca7b-dddc-4471-8a8a-6cb80608786a" />

thấy được là một chuyện, đọc đúng từng chữ là 1 chuyện khác, mình tốn 20 đến 30p chỉ để phân tích các kí tự đó 

và thu được 
```
WWWOIJWWOIJWWOIJWWaxwwxml

```

Mình để đó và phân tích tiếp file còn lại

<img width="1222" height="615" alt="image" src="https://github.com/user-attachments/assets/7e26458c-61e5-4e63-be3f-ac49a0d7a819" />
mình chỉ xài zsteg đơn giản là thấy 1 chuỗi lạ ở ảnh

khi xài mã hóa caesar và ở lần dịch thứ 8 nó ra 1 chuỗi hợp lí 

<img width="846" height="553" alt="image" src="https://github.com/user-attachments/assets/050e92ab-fc5c-44b7-93f8-c323d9048d38" />

tiếp tục với chuỗi còn lại 

<img width="896" height="468" alt="image" src="https://github.com/user-attachments/assets/b0af2f90-10bb-40ac-90c5-6568c36241ba" />

vấn đề ở cách ghép flag, tôi thử rất nhiều cách và cách cuối cùng đúng là 

```
spooky{OOOGABOOGABOOGABOOspoopedBOOgotyou}
