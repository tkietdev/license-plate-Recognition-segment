# Phát hiện và Nhận dạng Biển số xe Việt Nam (ALPR) bằng YOLOv8

Dự án ứng dụng mô hình **YOLOv8** để tự động hóa quy trình phát hiện và nhận dạng biển số xe tại Việt Nam. Đây là giải pháp hướng đến các ứng dụng thực tế như quản lý bãi đỗ xe thông minh, trạm thu phí tự động và giám sát giao thông.

---

## 📌 Tóm tắt dự án (Abstract)

Hệ thống xử lý hình ảnh đầu vào, xác định vị trí biển số xe và trích xuất nội dung văn bản thông qua quy trình gồm ba giai đoạn:

1. **Phát hiện (Detection):** Sử dụng YOLOv8 để xác định vị trí và khoanh vùng biển số xe (License Plate).
2. **Phân đoạn (Segmentation):** Tách các ký tự chữ và số từ vùng biển số đã được phát hiện.
3. **Nhận dạng (Recognition):** Phân loại từng ký tự và kết hợp chúng thành chuỗi văn bản hoàn chỉnh.

---

## 👨‍🏫 Thông tin đồ án

- **Giáo viên hướng dẫn:** Lê Quang Chiến
- **Sinh viên thực hiện:** Phan Hữu Tuấn Kiệt
- **Tên học phần:** Học máy và Python

---

## 📂 Cấu trúc thư mục (Project Structure)

```text
license-plate-Recognition-segment/
├── src/                        # Mã nguồn xử lý chính
│   ├── char_classification/    # Mô hình và logic phân loại ký tự
│   ├── lp_detection/           # Mô hình và logic phát hiện biển số
│   ├── weights/                # Trọng số mô hình YOLOv8 (.pt)
│   ├── data_utils.py           # Các hàm xử lý ảnh và vẽ khung
│   └── lp_recognition.py       # Module tích hợp nhận dạng biển số
├── sampledata/                 # Dữ liệu hình ảnh kiểm thử
├── app.py                      # Giao diện ứng dụng
├── main.py                     # Chương trình thực thi từ Terminal
├── requirements.txt            # Danh sách thư viện phụ thuộc
├── BaiDoAn.ipynb               # Notebook huấn luyện và thử nghiệm
└── data.zip                    # Bộ dữ liệu
```

---
