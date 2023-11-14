#**CRACKING LESSONS**

##**Crackme #5:**

- Tìm vị trí của dòng try again và lên trên 1 chút:
![](Images/Crackme_5_1.png)

- Ta thấy hàm GetDlgItemTextA để lấy text từ message box. Đặt breakpoint ở đó và xem xét bên dưới:
![](Images/Crackme_5_2.png)

- Sau khi step over đến dòng 0040116A, ta thấy chuỗi %s-%d…, đó là định dạng chuỗi – số, có thể đây là chỗ để generate key. Chạy them vài bước nữa, key sẽ được tạo ra, đó là sự kết hợp của tên người dung và chuỗi số cố định, là 32571021.
![](Images/Crackme_5_3.png)
