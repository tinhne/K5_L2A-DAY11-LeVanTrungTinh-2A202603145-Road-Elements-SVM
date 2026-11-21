# Phiếu QC 1 — Road v1.0

Lô được kiểm (học viên): Đinh Quang Thắng
Người kiểm (học viên): Lê Văn Trung Tính
Ngày: 21/11/2026
Phiên bản guideline: Road v1.0
File được kiểm (tên + revision trong manifest): DinhQuangThang-front.zip và fisheye.zip
Số ảnh kiểm: 6 (+ 0 ảnh thêm, ghi riêng)
Số nhãn đã kiểm (shape + tag): 58

## Tổng hợp theo mã

| Mã | Loại lỗi | Số mục kiểm | Số lỗi | Mức |
| --- | --- | ---: | ---: | --- |
| QC1-01 tag camera | sai thuộc tính / bỏ sót | 6 | 1 | nặng |
| QC1-02 đủ L1, R1 | bỏ sót | 6 | 5 | nặng |
| QC1-03 position | sai thuộc tính / thừa | 12 | 0 | nặng |
| QC1-04 tâm vạch, chiều, điểm dừng | sai phạm vi / bỏ sót | 12 | 0 | chính |
| QC1-05 vạch đứt, che | sai phạm vi / sai thuộc tính | 12 | 3 | chính |
| QC1-06 style, color, kind | sai thuộc tính | 12 | 0 | chính |
| QC1-07 vùng lái | sai phạm vi / bỏ sót / thừa | 22 | 0 | chính |
| QC1-08 đèn, màu | bỏ sót / sai phạm vi / sai thuộc tính | 0 | 0 | nặng / chính |
| QC1-09 facing, type, group, biển phụ | sai thuộc tính | 1 | 0 | chính |
| QC1-10 hình in, đủ biển | bỏ sót / sai phạm vi | 1 | 0 | chính |
| QC1-11 fisheye | sai phạm vi / sai thuộc tính | 18 | 0 | chính |
| QC1-12 file | lỗi file | 58 | 5 | nhẹ / nặng |

## Danh sách lỗi (mỗi lỗi một dòng)

| # | Mã | Ảnh | Nhãn (label, id) | Mức | Mô tả ngắn |
| --- | --- | --- | --- | --- | --- |
| 1 | QC1-01 | B02_03177_FV.png | tag camera, id 1 | nặng | Giá trị camera là `front`; tên hậu tố FV cần là `fisheye_front`. |
| 2 | QC1-02 | A05_b2576c8c-2de20b8a.jpg | lane, thiếu L1/R1 | nặng | Lint không tìm thấy L1 hoặc R1; cần coach xác nhận nếu ảnh không thật sự có vạch. |
| 3 | QC1-02 | A06_b8c66e31-37045eec.jpg | lane, thiếu R1 | nặng | Lint không tìm thấy R1; cần xác nhận vạch trên ảnh thật. |
| 4 | QC1-02 | B02_03177_FV.png | lane, thiếu L1/R1 | nặng | Không tìm thấy L1/R1 trên ảnh fisheye; cần xác nhận theo cảnh thực tế. |
| 5 | QC1-05 | A04_b7a8e795-0ff55db2.jpg | lane, id L1 | chính | Có 2 polyline cùng position L1; cần kiểm xem đó là hai đoạn của một vạch đứt hay hai vạch khác. |
| 6 | QC1-05 | A04_b7a8e795-0ff55db2.jpg | lane, id R2 | chính | Có 2 polyline cùng position R2; cần kiểm xem vạch đứt đã bị tách sai hay chưa. |
| 7 | QC1-05 | A08_c0deebc1-16cfa791.jpg | lane, id L1 | chính | Có 2 polyline cùng position L1; có thể là vạch đứt bị tách. |
| 8 | QC1-12 | A04_b7a8e795-0ff55db2.jpg | lane, id 1 | nhẹ | Có 1 cặp điểm trùng liền nhau; cần xoá điểm thừa. |
| 9 | QC1-12 | B02_03177_FV.png | crosswalk, drivable | nhẹ | Có điểm trùng liền nhau trong polygon; cần xoá điểm thừa. |
| 10 | QC1-12 | B04_05535_RV.png | crosswalk, drivable | nhẹ | Có điểm trùng liền nhau trong polygon; cần xoá điểm thừa. |

## Ca mơ hồ

| Ảnh | Câu hỏi cho lead | Lời đáp (nếu có) |
| --- | --- | --- |
| A05 | L1/R1 có thật sự không xuất hiện hay lint chỉ chưa ghép lane? | Chưa có |
| A06 | R1 có thật sự nhìn không thấy không? | Chưa có |
| B02 | Ảnh có lane nhưng L1/R1 không nhìn rõ ở đoạn nào? | Chưa có |

## Quyết định

Lỗi nặng: 6
Lỗi chính: 3 / 58 nhãn = 5.17%
Lỗi nhẹ: 5
Ca chờ lead: 3
Quyết định (Release / Hold / Rework): Rework
Lý do (theo luật của phiếu): Có lỗi nặng tag camera sai và còn các cảnh báo thiếu lane chưa được xác nhận. Ngay cả khi A05/A06/B02 được miễn theo trường hợp coach xác nhận không thấy vạch, vẫn còn lỗi nặng QC1-01; theo luật phiếu phải Rework.
