#**CRACKING LESSONS**

##**Crackme #10:**

- Nó cố gắng đọc file keyfile.dat:
![](Images/Crackme_10_1.png)

- Giá trị eax sau lệnh CreateFileA là FFFFFFFF (là số âm), tức là không tìm thấy file. Ta cần tạo file Keyfile.dat để đọc được file.
![](Images/Crackme_10_2.png)

- Dòng 004010B8 có lệnh so sánh ở ô 402173 với 0x10 (là 16), như vậy key có 16 kí tự.
- Tiếp theo có 1 vòng lặp cho đến khi thấy sign 0, tức là phần cuối của file.
- Vòng lặp này đếm số lần kí tự G xuất hiện vào biến đếm esi. Sau đó nó có lệnh cmp esi, 8, tức là nếu esi < 8 thì nó sẽ nhảy đến not valid. Điều này cho thấy key phải có 8 kí tự G và dài 16 kí tự.
Ta hãy cho 1 pass vào file .dat ở trên, ví dụ GGGGGGGG12345678 (đủ 16 kí tự và 8 chữ G):
![](Images/Crackme_10_3.png)