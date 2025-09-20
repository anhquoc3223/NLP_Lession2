# Ứng Dụng Phân Tích Văn Bản

Ứng dụng web toàn diện để phân tích văn bản sử dụng các kỹ thuật Xử lý Ngôn ngữ Tự nhiên (NLP). Ứng dụng này minh họa pipeline NLP cổ điển: **Tách từ → Gắn nhãn từ loại → Nhận dạng thực thể có tên**.

## 🚀 Tính Năng

- **Tách từ (Tokenization)**: Chia văn bản thành các từ đơn lẻ (từ, dấu câu, v.v.)
- **Gắn nhãn từ loại (POS Tagging)**: Xác định các loại từ ngữ pháp của mỗi token
- **Nhận dạng thực thể có tên (NER)**: Trích xuất và phân loại các thực thể có tên (người, tổ chức, địa điểm, v.v.)
- **Trực quan hóa tương tác**: Biểu đồ và đồ thị để hiểu rõ hơn
- **Tô màu thực thể**: Biểu diễn trực quan các loại thực thể khác nhau
- **Thống kê toàn diện**: Tóm tắt phân tích chi tiết với các chỉ số

## 🛠️ Công Nghệ Sử Dụng

- **spaCy**: Thư viện NLP tiên tiến cho tách từ, gắn nhãn từ loại và NER
- **Streamlit**: Framework web hiện đại để tạo ứng dụng dữ liệu tương tác
- **Pandas**: Thao tác và phân tích dữ liệu
- **Plotly**: Trực quan hóa tương tác và biểu đồ

## 📋 Yêu Cầu Hệ Thống

- Python 3.7 trở lên
- pip (trình cài đặt gói Python)

## 🔧 Cài Đặt

1. **Clone hoặc tải xuống dự án này**
   ```bash
   cd /path/to/your/project
   ```

2. **Cài đặt các phụ thuộc Python**
   ```bash
   pip install -r requirements.txt
   ```

3. **Tải xuống mô hình tiếng Anh của spaCy**
   ```bash
   python -m spacy download en_core_web_sm
   ```

## 🚀 Chạy Ứng Dụng

1. **Khởi động ứng dụng Streamlit**
   ```bash
   streamlit run app.py
   ```

2. **Mở trình duyệt web**
   - Ứng dụng sẽ tự động mở tại `http://localhost:8501`
   - Nếu không tự động mở, hãy điều hướng thủ công đến URL hiển thị trong terminal

## 📖 Cách Sử Dụng

### 1. Nhập Văn Bản
- **Tùy chọn A**: Nhập văn bản của bạn vào ô nhập liệu ở sidebar bên trái
- **Tùy chọn B**: Chọn một trong các văn bản mẫu có sẵn từ menu dropdown

### 2. Phân Tích Văn Bản
- Nhấn nút **"🔍 Phân Tích Văn Bản"** để xử lý văn bản đầu vào

### 3. Xem Kết Quả
Ứng dụng cung cấp bốn tab chính:

#### 🔤 Tab Tách Từ
- Hiển thị tất cả các token riêng lẻ được trích xuất từ văn bản
- Hiển thị thuộc tính token (khoảng trắng, chữ cái, số, dấu câu)
- Cung cấp thống kê token (tổng token, từ, số, dấu câu)

#### 🏷️ Tab Gắn Nhãn Từ Loại
- Hiển thị nhãn Part-of-Speech cho mỗi token
- Hiển thị cả nhãn thô và nhãn chi tiết
- Bao gồm lemmatization (dạng gốc của từ)
- Hiển thị biểu đồ phân bố nhãn POS

#### 👥 Tab Nhận Dạng Thực Thể
- Liệt kê tất cả các thực thể có tên được tìm thấy trong văn bản
- Phân loại thực thể theo loại (PERSON, ORG, GPE, v.v.)
- Cung cấp biểu đồ tròn phân bố loại thực thể
- **Tô màu các thực thể trong văn bản gốc với các màu khác nhau**

#### 📊 Tab Tổng Kết
- Thống kê tổng quan về văn bản (ký tự, từ, câu)
- Các chỉ số tóm tắt thực thể
- Biểu đồ từ xuất hiện nhiều nhất
- Độ dài từ trung bình và các thông tin khác

## 🎨 Mã Màu Thực Thể

Ứng dụng sử dụng các màu khác nhau để tô màu các loại thực thể:

- **PERSON** (Người): Đỏ
- **ORG** (Tổ chức): Xanh ngọc
- **GPE** (Thực thể địa chính trị): Xanh dương
- **LOC** (Địa điểm): Xanh lá
- **DATE** (Ngày tháng): Vàng
- **TIME** (Thời gian): Tím
- **MONEY** (Tiền tệ): Xanh bạc hà
- **PERCENT** (Phần trăm): Vàng nhạt
- Và nhiều loại khác...

## 📊 Văn Bản Mẫu

Ứng dụng bao gồm ba văn bản mẫu để bạn bắt đầu:

1. **Bài báo tin tức**: Về Apple Inc. và Tim Cook
2. **Văn bản khoa học**: Về nghiên cứu từ MIT
3. **Báo cáo kinh doanh**: Về thu nhập của Microsoft

## 🔍 Hiểu Kết Quả

### Tách Từ
- **Token**: Các đơn vị riêng lẻ của văn bản (từ, dấu câu, khoảng trắng)
- **Khoảng trắng**: Token có theo sau bởi khoảng trắng hay không
- **Chữ cái**: Token có chứa chỉ các ký tự chữ cái hay không
- **Số**: Token có chứa chỉ các chữ số hay không
- **Dấu câu**: Token có phải là dấu câu hay không

### Gắn Nhãn Từ Loại
- **Nhãn POS**: Loại ngữ pháp thô (NOUN, VERB, ADJ, v.v.)
- **Nhãn chi tiết**: Thông tin ngữ pháp cụ thể hơn
- **Lemma**: Dạng gốc của từ (ví dụ: "running" → "run")
- **Từ dừng**: Các từ phổ biến thường được lọc bỏ (the, a, an, v.v.)

### Nhận Dạng Thực Thể Có Tên
- **PERSON**: Tên người
- **ORG**: Tổ chức, công ty, cơ quan
- **GPE**: Quốc gia, thành phố, bang (thực thể địa chính trị)
- **LOC**: Địa điểm phi địa chính trị (núi, sông, hồ)
- **DATE**: Ngày tháng tuyệt đối hoặc tương đối
- **TIME**: Thời gian nhỏ hơn một ngày
- **MONEY**: Giá trị tiền tệ
- **PERCENT**: Phần trăm
- **CARDINAL**: Số đếm không thuộc các loại khác
- **ORDINAL**: "first", "second", v.v.

## 🐛 Khắc Phục Sự Cố

### Các Vấn Đề Thường Gặp

1. **Lỗi "spaCy English model not found"**
   ```bash
   python -m spacy download en_core_web_sm
   ```

2. **Lỗi không tìm thấy module**
   ```bash
   pip install -r requirements.txt
   ```

3. **Cổng đã được sử dụng**
   - Streamlit sẽ tự động tìm cổng khả dụng
   - Hoặc chỉ định cổng khác: `streamlit run app.py --server.port 8502`

## 📁 Cấu Trúc Dự Án

```
lesson_2/
├── app.py              # Ứng dụng Streamlit chính
├── requirements.txt    # Các phụ thuộc Python
└── README.md          # Tệp này
```

## 🎯 Mục Tiêu Học Tập

Ứng dụng này minh họa:

1. **Tiền xử lý văn bản**: Cách làm sạch và chuẩn bị văn bản để phân tích
2. **Tách từ**: Chia văn bản thành các đơn vị có ý nghĩa
3. **Phân tích ngôn ngữ**: Hiểu cấu trúc ngữ pháp
4. **Trích xuất thông tin**: Xác định các thực thể quan trọng trong văn bản
5. **Trực quan hóa dữ liệu**: Trình bày kết quả NLP hiệu quả
6. **Phát triển ứng dụng web**: Tạo công cụ NLP tương tác

## 🔮 Cải Tiến Tương Lai

Các cải tiến tiềm năng bạn có thể thêm:

- Hỗ trợ nhiều ngôn ngữ
- Phân tích cảm xúc
- Tóm tắt văn bản
- Trực quan hóa phân tích cú pháp phụ thuộc
- Nhận dạng thực thể tùy chỉnh
- Xuất kết quả ra CSV/JSON
- Xử lý hàng loạt nhiều văn bản

## 📚 Tài Liệu Tham Khảo

- [Tài liệu spaCy](https://spacy.io/usage)
- [Tài liệu Streamlit](https://docs.streamlit.io/)
- [Xử lý Ngôn ngữ Tự nhiên với Python](https://www.nltk.org/book/)

## 🤝 Đóng Góp

Hãy thoải mái fork dự án này và thêm các tính năng hoặc cải tiến của riêng bạn!

---

**Chúc bạn phân tích văn bản vui vẻ! 📝✨**
