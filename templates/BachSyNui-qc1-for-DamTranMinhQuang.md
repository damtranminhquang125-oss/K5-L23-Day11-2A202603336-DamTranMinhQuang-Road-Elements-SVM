# Phiếu QC 1 — Road v1.0

Lô được kiểm (học viên): Đàm Trần Minh Quang        Người kiểm (học viên): Bạch Sỹ Núi
Ngày: 21/11/2026                         Phiên bản guideline: Road v1.0  
File được kiểm (tên + `revision` trong manifest): DamTranMinhQuang_revision 
Số ảnh kiểm: 20 (+ 0 ảnh thêm, ghi riêng)   Số nhãn đã kiểm (shape + tag):  

## Tổng hợp theo mã
| Mã | Loại lỗi | Số mục kiểm | Số lỗi | Mức |
| --- | --- | ---: | ---: | --- |
| QC1-01 tag camera | sai thuộc tính / bỏ sót | — | 0 | nặng |
| QC1-02 đủ L1, R1 | bỏ sót | — | 6 | nặng |
| QC1-03 position | sai thuộc tính / thừa | — | 0 | nặng |
| QC1-04 tâm vạch, chiều, điểm dừng | sai phạm vi / bỏ sót | — | 3 | chính |
| QC1-05 vạch đứt, che | sai phạm vi / sai thuộc tính | — | 3 | chính |
| QC1-06 style, color, kind | sai thuộc tính | — | 0 | chính |
| QC1-07 vùng lái | sai phạm vi / bỏ sót / thừa | — | 0 | chính |
| QC1-08 đèn, màu | bỏ sót / sai phạm vi / sai thuộc tính | — | 0 | nặng / chính |
| QC1-09 facing, type, group, biển phụ | sai thuộc tính | — | 0 | chính |
| QC1-10 hình in, đủ biển | bỏ sót / sai phạm vi | — | 1 | nhẹ |
| QC1-11 fisheye | sai phạm vi / sai thuộc tính | — | 3 | chính |
| QC1-12 file | lỗi file | — | 0 | nhẹ |

Tổng cộng: 16 cảnh báo (6 nặng, 9 chính, 1 nhẹ).

## Danh sách lỗi (mỗi lỗi một dòng)
| # | Mã | Ảnh | Nhãn (label, id) | Mức | Mô tả ngắn |
| --- | --- | --- | --- | --- | --- |
| 1 | QC1-04 | A03 | lane#2@(594,385) | chính | Điểm đầu cao hơn điểm cuối; kiểm tra chiều vẽ từ xa về gần. |
| 2 | QC1-04 | A03 | lane#3@(685,397) | chính | Điểm đầu cao hơn điểm cuối; kiểm tra chiều vẽ từ xa về gần. |
| 3 | QC1-05 | A04 | lane, position L1 | chính | Có 2 polyline cùng position L1; kiểm tra vạch đứt có bị tách không. |
| 4 | QC1-02 | A05 | lane, L1 | nặng | Chưa có L1; bỏ qua nếu thật sự không thấy vạch. |
| 5 | QC1-02 | A05 | lane, R1 | nặng | Chưa có R1; bỏ qua nếu thật sự không thấy vạch. |
| 6 | QC1-02 | A06 | lane, R1 | nặng | Chưa có R1; bỏ qua nếu thật sự không thấy vạch. |
| 7 | QC1-02 | A07 | lane, L1 | nặng | Chưa có L1; bỏ qua nếu thật sự không thấy vạch. |
| 8 | QC1-02 | A08 | lane, L1 | nặng | Chưa có L1; bỏ qua nếu thật sự không thấy vạch. |
| 9 | QC1-02 | A09 | lane, R1 | nặng | Chưa có R1; bỏ qua nếu thật sự không thấy vạch. |
| 10 | QC1-05 | A09 | lane, position L2 | chính | Có 2 polyline cùng position L2; kiểm tra vạch đứt có bị tách không. |
| 11 | QC1-10 | A10 | traffic_sign#6@(423,192) | nhẹ* | Box thấp hơn 8 px; không bắt buộc, chỉ là gợi ý tự kiểm. |
| 12 | QC1-05 | A11 | lane, position L1 | chính | Có 2 polyline cùng position L1; kiểm tra vạch đứt có bị tách không. |
| 13 | QC1-04 | A12 | lane#4@(603,392) | chính | Điểm đầu cao hơn điểm cuối; kiểm tra chiều vẽ từ xa về gần. |
| 14 | QC1-11 | B03 | traffic_sign#10@(174,300) | chính | Lint gợi ý tắt `edge_zone`; tự kiểm tra lại theo vị trí box. |
| 15 | QC1-11 | B03 | traffic_sign#11@(259,292) | chính | Lint gợi ý tắt `edge_zone`; tự kiểm tra lại theo vị trí box. |
| 16 | QC1-11 | B03 | traffic_sign#12@(1001,278) | chính | Lint gợi ý tắt `edge_zone`; tự kiểm tra lại theo vị trí box. |

## Ca cần người kiểm xác nhận
| Ảnh | Câu hỏi cho lead | Lời đáp (nếu có) |
| --- | --- | --- |
| A05-A09 | Các cảnh báo thiếu L1/R1 có phải vạch nhìn thấy trong GT không? | Không |
| A04, A09, A11 | Các polyline trùng position có phải vạch đứt bị tách không? | Có |
| B03 | Các box biển có nằm trong vùng cần `edge_zone` không? | Vài cái chưa gán |

## Quyết định
Lỗi nặng/chính/nhẹ đã xác nhận: 6 / 9 / 1.  
Tỷ lệ lỗi chính: 3 (chưa có số nhãn và lỗi được xác nhận).
Quyết định (Release / Hold / Rework): Release. 
Lý do: cần kiểm tra thêm cho trực quan và đối chiếu ground truth.

Loại lỗi: bỏ sót = thiếu nhãn phải có; thừa = gán cái không phải đối tượng; sai phạm vi = hình lệch, sai chiều, dừng sai chỗ, tràn vùng. Ba loại này theo cách chia lỗi gán nhãn của ISO/IEC 5259-4 (mục 8.4.2); "sai thuộc tính" và "lỗi file" là khóa học thêm. Cách xếp mức: [thang mức lỗi](../docs/qc_severity_road_v1.0.md).
