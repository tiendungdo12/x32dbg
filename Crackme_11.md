#**CRACKING LESSONS**

##**Crackme #11:**

- Trước hết, ta cần unpack file bằng lệnh upx -d -o lab11.exe CrackMe11-packed.exe, thu được file Unpacked như đã tải.
Chỉ cần tìm string references, ta tìm được dòng thông báo:
![](Images/Crackme_11_1.png)

- Ta chỉ cần sửa je thành jmp để nhảy xuống bên dưới là patch thành công:
![](Images/Crackme_11_2.png)