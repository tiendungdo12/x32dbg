#**CRACKING LESSONS**

##**Crackme #3:**

- Đi đến nơi có thông báo đầu tiên:
![](Images/Crackme_3_1.png)

- Ở dòng 00401029 có 1 lệnh jump dựa theo việc so sánh ở dòng 0040101D để hiện messagebox ở dòng 00401039.
Ta chỉ cần sửa jne thành je để bypass box đầu.
![](Images/Crackme_3_2.png)

- Ở đây đã skip box đầu, giờ tìm vị trí box 2.
![](Images/Crackme_3_3.png)

- Giữa MessageBoxA và PostQuitMessage (là vùng để hiện dialog 2), ta cần jump đến vị trí đó, nhưng do không có lệnh jump sẵn nên ta cần tự set jump command. Ta sửa dòng 0040110D thành push 0x401121, và pass được box 2:
![](Images/Crackme_3_4.png)

- Ở đoạn registered, ta thấy dòng 004010D8 có lệnh je dựa trên lệnh compare eax ngay trên. Ta sửa thành jne để nó không jump xuống dòng unregistered (cho giá trị khác nhau).
![](Images/Crackme_3_5.png)