# ĐỒ ÁN 1 - NHẬN DẠNG LỆNH THOẠI BẰNG MATLAB

**Môn học:** Xử lý tín hiệu số  
**Nhóm:** 6  
**Phương pháp:** Tương quan chéo  
**Mã nguồn chính:** `DoAn1_NhanDangLenhThoai_Nhom6.mlx`

## Thành viên

| STT | Họ và tên | MSSV |
|---:|---|---:|
| 1 | Huỳnh Tấn Phát | 24200144 |
| 2 | Lưu Hữu Phước | 24200150 |
| 3 | Đặng Văn Trung | 24200192 |
| 4 | Trương Công Vinh | 24200204 |
| 5 | Phan Thành Nhân | 24200140 |
| 6 | Nguyễn Thanh Tuấn | 24200199 |
| 7 | Vàng Minh Trương | 24200193 |

## Kiến trúc đồ án

Toàn bộ quy trình được thực hiện trong một MATLAB Live Script duy nhất:

```text
Nhấn Enter
    -> MATLAB thu Open
    -> MATLAB thu Close
    -> MATLAB thu testSample
    -> Vẽ dạng sóng
    -> Nhận dạng bằng xcorr()
    -> Tính năng lượng
    -> Thêm nhiễu Gaussian tại SNR 10 dB
    -> Kiểm thử 100 lần
    -> Tiền xử lý và tương quan chéo chuẩn hóa
    -> Hiển thị kết quả
```



## Cách chạy

1. Mở `DoAn1_NhanDangLenhThoai_Nhom6.mlx` bằng MATLAB.
2. Chọn **Run All**.
3. Khi chương trình yêu cầu lệnh `Open`, chuẩn bị phát âm rồi nhấn Enter.
4. Chỉ bắt đầu nói khi dòng `DANG GHI AM` xuất hiện.
5. Thực hiện tương tự cho lệnh `Close` và mẫu kiểm tra.
6. Nhập nhãn thật của mẫu kiểm tra nếu biết. Có thể nhấn Enter để bỏ qua.
7. Chờ chương trình hoàn tất phần kiểm thử 100 lần.
8. Xem kết quả, biểu đồ dạng sóng, biểu đồ nhiễu và biểu đồ so sánh ngay trong Live Script.

## Nội dung thực hiện

- Thu âm ở 44.100 Hz, 16 bit, mono, thời lượng 2 giây.
- Nhận dạng `Open` hoặc `Close` bằng đỉnh tương quan chéo.
- Tính năng lượng theo `E = sum(x[n]^2)`.
- Sinh nhiễu Gaussian có năng lượng bằng chính xác `1/10` năng lượng tín hiệu.
- Xác nhận SNR bằng 10 dB.
- Kiểm tra khả năng nhận dạng `Open` và `Close` sau khi thêm nhiễu.
- Lặp 100 lần với các dãy nhiễu độc lập.
- Đề xuất cải tiến bằng lọc thông dải, cắt khoảng lặng và tương quan chéo chuẩn hóa.

## Lưu ý khi chạy

- Chương trình không lưu bản ghi ra ổ đĩa. Nếu đóng MATLAB hoặc chạy lại từ đầu, cần thu lại ba tín hiệu.
- Nên thu trong phòng yên tĩnh và giữ khoảng cách tới microphone tương đối ổn định.
- Mỗi từ phải được phát âm sau khi MATLAB bắt đầu ghi và nằm trong khoảng 2 giây.
- Kết quả số thay đổi theo giọng nói, microphone và môi trường của từng lần chạy.

## Giới hạn đánh giá

Phần kiểm thử nhiễu sử dụng chính hai mẫu `Open` và `Close` làm mẫu chuẩn rồi thêm nhiễu vào chúng. Kết quả này đánh giá độ ổn định trên hai bản ghi hiện tại.



