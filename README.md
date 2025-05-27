
# So sánh phổ âm thanh giữa nhạc cổ điển và nhạc điện tử

## Mô tả dự án

Dự án này thực hiện phân tích và so sánh phổ tần số của hai thể loại nhạc:
- **Nhạc cổ điển**: Beethoven, Brahms, Mozart, Liszt
- **Nhạc điện tử**: Album "Esp"

## Dữ liệu sử dụng
Tổng cộng 15 file WAV (đã chuyển đổi từ MIDI):

### Nhạc cổ điển (12 file):
- `mz_311_1.wav`, `mz_311_2.wav`, `mz_311_3.wav`
- `brahms_opus1_1.wav`, `brahms_opus1_2.wav`, `brahms_opus1_3.wav`
- `beethoven_les_adieux_1.wav`, `beethoven_les_adieux_2.wav`, `beethoven_les_adieux_3.wav`
- `liz_et1.wav`, `liz_et2.wav`, `liz_et3.wav`

### Nhạc điện tử (3 file):
- `alb_esp1.wav`, `alb_esp2.wav`, `alb_esp3.wav`

## Tiền xử lý

- Đọc 5 giây đầu tiên của mỗi tệp âm thanh.
- Giảm đa kênh về mono nếu cần.
- Chuẩn hóa biên độ.
- Thực hiện FFT (Biến đổi Fourier nhanh) bằng NumPy.
- Giới hạn phổ ở mức 4000 Hz để dễ so sánh.

## Phân tích

- Tính **trung bình phổ biên độ** của từng thể loại nhạc.
- Vẽ biểu đồ so sánh.

## Kết quả

- Nhạc cổ điển chủ yếu tập trung vào dải tần thấp đến trung (dưới 1500 Hz).
- Nhạc điện tử trải rộng phổ hơn, có năng lượng ở cả vùng tần số cao (trên 2000 Hz).
- Có thể sử dụng phổ trung bình như đặc trưng để phân loại thể loại nhạc.


