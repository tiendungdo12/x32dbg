#**CRACKING LESSONS**

##**Crackme #13:**

![](Images/Crackme_13_1.png)
- Tiếp tục như bài 12, sửa je thành jmp để bypass anti-debugging. 
![](Images/Crackme_13_2.png)

- Sửa tiếp để pass bước sai key.
Và ta export ra dạng .1337 để lưu lại vị trí patch:
![](Images/Crackme_13_3.png)

- Việc còn lại là patch serial key bằng cách tạo loader file, ở đây ta sử dụng DUP2 từ trang của crackinglessons.
![](Images/Crackme_13_4.png)

+ Tạo 1 project mới từ file ban đầu:
![](Images/Crackme_13_5.png)

+ Tạo thêm offset patch:
![](Images/Crackme_13_6.png)

+ Edit offset patch: (Chọn RVA và điền offset từ file .1337 ở trên)
![](Images/Crackme_13_7.png)

+ Tạo 1 simple loader (project -> create loader):
![](Images/Crackme_13_8.png)