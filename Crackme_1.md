#**CRACKING LESSONS**

##**Crackme #1:**

- Sử dụng DIE để check address của entry point là 004013bf.
![](Images/Crackme_1_1.png)

- Mở x32dbg, run và xác nhận entry point.
![](Images/Crackme_1_2.png)

- Khi run tiếp thì sẽ ra cửa sổ nhập pass, việc cần làm là break. Ta tìm các string references và tìm location của chuỗi thông báo “try again”:
![](Images/Crackme_1_3.png)

- Nhìn ngay trên có thông báo congrats, và đây là thông báo mà ta muốn hiển thị.
![](Images/Crackme_1_4.png)

- Có 1 tham chiếu GetDIgItemTextA để lấy item từ text nhập pass. Dòng 00401139 có 1 conditional jump, dựa theo dòng test eax ở trên để compare với “cr4ckingL3ssons”, nếu eax = 0 thì dòng congrats được hiển thị, ngược lại sẽ nhảy đến thông báo sai. Như vậy pass là cr4ckingL3ssons.
![](Images/Crackme_1_5.png)

- Để luôn hiển thị dialog well done, ta cần sửa giá trị của eax thành 0 để luôn đúng.
![](Images/Crackme_1_6.png)

- Patch file và chạy thử:
![](Images/Crackme_1_7.png)
