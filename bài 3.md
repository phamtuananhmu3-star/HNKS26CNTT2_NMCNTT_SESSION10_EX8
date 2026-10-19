### **Phần 1: Phân tích lỗi**

1.  **Vi phạm Quy tắc 1 :** Hàng tiêu đề bị trộn ô (Merge) và đặt trên header, làm AutoFilter nhận diện sai vùng dữ liệu.
    
2.  **Vi phạm Quy tắc 4 :** Dòng _"TỔNG SỐ CNTT: 45"_ chèn ngang bảng làm ngắt quãng phạm vi lọc của AutoFilter.
    
3.  **Vi phạm Quy tắc 2 & 3 :** Ô `B3` chứa khoảng trắng thừa (`Trần Thị Bình` ), khiến bộ lọc không khớp chuỗi chính xác.
    

### **Phần 2: Sửa lỗi & Nghiệm thu**

1.  **Cấu trúc chuẩn:**
    
    -   Xóa dòng tiêu đề merge và đưa dòng tổng kết ra ngoài/xuống dưới cùng.
        
    -   Header chuẩn ở hàng đầu: `STT | Họ và Tên | Khoa / Viện | Điểm Xét Duyệt | Trạng Thái`.
        
2.  **Làm sạch & Lọc dữ liệu:**
    
    -   Dùng cột phụ với hàm xóa khoảng trắng: `=TRIM(B3)` sang  Copy và Paste Values đè lại cột Họ và Tên.
        
    -   Bôi đen bảng xong nhấn `Ctrl + Shift + L` sang Lọc Khoa = `CNTT` và Điểm $\ge 8.0$
