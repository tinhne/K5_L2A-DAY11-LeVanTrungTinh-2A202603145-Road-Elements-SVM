# Phiếu QC 1 — Road v1.0

Lô được kiểm (học viên): LÊ VĂN TRUNG TÍNH
Người kiểm (học viên): ĐINH QUANG THẮNG
Ngày: 21/11/2026
Phiên bản guideline: Road v1.0
File được kiểm (tên + `revision` trong manifest): LeVanTrungTinh-front.zip và LeVanTrungTinh-fisheye.zip
Số ảnh kiểm: 12 (+ 0 ảnh thêm, ghi riêng)
Số nhãn đã kiểm (shape + tag): 109

## Tổng hợp theo mã
| Mã | Loại lỗi | Số mục kiểm | Số lỗi | Mức |
| --- | --- | ---: | ---: | --- |
| QC1-01 tag camera | sai thuộc tính / bỏ sót | 12 | 0 | nặng |
| QC1-02 đủ L1, R1 | bỏ sót | 12 | 8 | nặng |
| QC1-03 position | sai thuộc tính / thừa | 8 | 0 | nặng |
| QC1-04 tâm vạch, chiều, điểm dừng | sai phạm vi / bỏ sót | 8 | 0 | chính |
| QC1-05 vạch đứt, che | sai phạm vi / sai thuộc tính | 8 | 1 | chính |
| QC1-06 style, color, kind | sai thuộc tính | 8 | 0 | chính |
| QC1-07 vùng lái | sai phạm vi / bỏ sót / thừa | 21 | 0 | chính |
| QC1-08 đèn, màu | bỏ sót / sai phạm vi / sai thuộc tính | 8 | 0 | nặng / chính |
| QC1-09 facing, type, group, biển phụ | sai thuộc tính | 8 | 0 | chính |
| QC1-10 hình in, đủ biển | bỏ sót / sai phạm vi | 0 | 0 | chính |
| QC1-11 fisheye | sai phạm vi / sai thuộc tính | 6 | 0 | chính |
| QC1-12 file | lỗi file | 2 | 0 | nhẹ / nặng |

## Danh sách lỗi (mỗi lỗi một dòng)
| # | Mã | Ảnh | Nhãn (label, id) | Mức | Mô tả ngắn |
| --- | --- | --- | --- | --- | --- |
| 1 | QC1-02 | A03_b1c66a42-6f7d68ca.jpg | lane, R1 | nặng | Thiếu làn chủ đạo bên phải R1 |
| 2 | QC1-05 | A03_b1c66a42-6f7d68ca.jpg | lane, id L1 tách thành 2 | chính | Vạch đứt L1 bị gán thành hai polyline |
| 3 | QC1-02 | B01_02688_FV.png | lane, L1 | nặng | Thiếu làn chủ đạo bên trái L1 |
| 4 | QC1-02 | B01_02688_FV.png | lane, R1 | nặng | Thiếu làn chủ đạo bên phải R1 |
| 5 | QC1-02 | B02_03177_FV.png | lane, L1 | nặng | Thiếu làn chủ đạo bên trái L1 |
| 6 | QC1-02 | B02_03177_FV.png | lane, R1 | nặng | Thiếu làn chủ đạo bên phải R1 |
| 7 | QC1-02 | B03_04267_RV.png | lane, L1 | nặng | Thiếu làn chủ đạo bên trái L1 |
| 8 | QC1-02 | B04_05535_RV.png | lane, R1 | nặng | Thiếu làn chủ đạo bên phải R1 |

## Ca mơ hồ
| Ảnh | Câu hỏi cho lead | Lời đáp (nếu có) |
| --- | --- | --- |
| A05_b2576c8c-2de20b8a.jpg | Có thấy đủ L1/R1 trên ảnh front hay thực sự không có vạch? | Chưa có lead xác nhận |
| A06_b8c66e31-37045eec.jpg | Có thấy đủ L1/R1 tại ngã giao hay thực sự không có vạch chủ đạo? | Chưa có lead xác nhận |
| B02_03177_FV.png | Ba box đèn/đèn hướng ở mép ảnh có thuộc tính type/facing/color và box nào đúng là cần xác nhận? | Chưa có lead xác nhận |

## Quyết định
Lỗi nặng: 8   Lỗi chính: 1 / 109 nhãn = 0.92 %   Lỗi nhẹ: 0   Ca chờ lead: 3
Quyết định (Release / Hold / Rework): Rework
Lý do (theo luật của phiếu): Có 8 lỗi nặng do bỏ sót L1/R1; lỗi chính 1/109 nhãn = 0.92% chưa vượt 5%, nhưng có ít nhất một lỗi nặng nên lô phải Rework.

Loại lỗi: bỏ sót = thiếu nhãn phải có; thừa = gán cái không phải đối tượng; sai phạm vi = hình lệch, sai chiều, dừng sai chỗ, tràn vùng. Ba loại này theo cách chia lỗi gán nhãn của ISO/IEC 5259-4 (mục 8.4.2); "sai thuộc tính" và "lỗi file" là khóa học thêm. Cách xếp mức: [thang mức lỗi](../docs/qc_severity_road_v1.0.md).
