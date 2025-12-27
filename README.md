# 🎮 Phân Tích Dữ Liệu Doanh Số Bán Game Toàn Cầu

## Mô tả đồ án

Đồ án này phân tích dataset doanh số bán video game toàn cầu từ VGChartz, với hơn 16,000 game được phát hành từ những năm 1980 đến 2020. Mục tiêu là khám phá các xu hướng thị trường, phân tích các yếu tố ảnh hưởng đến doanh số, và xây dựng model dự đoán doanh số game.

**Link dataset:** https://www.kaggle.com/datasets/gregorut/videogamesales

## 👥 Thông tin nhóm

| STT | Họ và Tên | MSSV | 
|-----|-----------|------|
| 1 | Bàng Mỹ Linh | 23122009 | 
| 2 | Nguyễn Gia Bảo | 23122015 | 
| 3 | Lại Nguyễn Hồng Thanh | 23122018 | 

## Cấu trúc thư mục

```
Group_19/
│
├── README.md                                    # File mô tả project
├── Team_Plan_Work_Distribution.pdf              # Kế hoạch và phân công công việc
├── data/
│   └── vgsales.csv                              # Dataset gốc từ Kaggle
└── notebooks/
  ├── 01_Data_Collection_Preprocessing_EDA.ipynb   # Thu thập, tiền xử lý & EDA
  ├── 02_Analysis_Questions.ipynb                  # Phân tích câu hỏi 1-5
  └── 03_Modeling.ipynb                            # Machine Learning & Kết luận
```

## 📓 Mô tả các Notebook

### Notebook 1: Data Collection, Preprocessing & EDA
- **Nội dung:** Thu thập dữ liệu, tiền xử lý và khám phá dữ liệu chi tiết
- **Bao gồm:**
  - Giới thiệu dataset và nguồn gốc dữ liệu
  - Kiểm tra dữ liệu thiếu và trùng lặp
  - Phân tích theo Platform, Genre, Year, Publisher
  - Phân tích doanh số theo khu vực địa lý
  - Phân tích tương quan và phân phối dữ liệu
  - Đánh giá chất lượng dữ liệu

### Notebook 2: Analysis Questions (Câu 1-6)
- **Nội dung:** Trả lời 5 câu hỏi phân tích chính và 1 câu hỏi dùng machine learning model.
- **Các câu hỏi:**
  1. Sự kết hợp Platform-Genre nào mang lại doanh số trung bình cao nhất?
  2. Doanh số game thay đổi như thế nào theo vòng đời của nền tảng?
  3. Thể loại game nào đang tăng trưởng/suy giảm theo thời gian?
  4. Publisher nào có tỷ lệ tạo ra "hit game" cao nhất?
  5. Có sự khác biệt về hiệu suất giữa publisher lớn và nhỏ không?
  6. Có thể dự đoán doanh số của game dựa trên các thuộc tính không? (modeling)

### Notebook 3: Modeling & Conclusion
- **Nội dung:** Xây dựng model ML dự đoán doanh số game (câu hỏi 6) và kết luận
- **Bao gồm:**
  - Chuẩn bị dữ liệu cho Machine Learning
  - Huấn luyện và so sánh 3 models (Linear Regression, Random Forest, Gradient Boosting)
  - Đánh giá model với MAE, Median AE, RMSE, Cross-validation
  - Phân tích Feature Importance
  - Kết luận và những khó khăn gặp phải
  - Tài liệu tham khảo

## 🛠️ Cài đặt và Chạy

### Yêu cầu
- Python 3.8+
- Jupyter Notebook

### Thư viện cần thiết
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Hướng dẫn chạy
1. Clone hoặc download project
2. Download dataset `vgsales.csv` từ Kaggle và đặt vào thư mục `data/`
3. Mở và chạy các notebook theo thứ tự:
   - `01_Data_Collection_Preprocessing_EDA.ipynb`
   - `02_Analysis_Questions.ipynb`
   - `03_Modeling.ipynb`

## Kết quả chính

### Những phát hiện quan trọng:
- **Platform-Genre tốt nhất:** Wii + Sports/Platform có doanh số trung bình cao nhất
- **Thời điểm phát hành:** Giai đoạn đầu vòng đời platform mang lại doanh số tốt nhất
- **Xu hướng Genre:** Shooter tăng trưởng mạnh nhất, Platform và Racing suy giảm
- **Publisher hiệu quả:** Nintendo có tỷ lệ hit cao nhất (~65%)
- **Model dự đoán:** Gradient Boosting đạt MAE ~0.5 triệu USD

### Feature Importance:
1. Year (35%) - Thời điểm phát hành quan trọng nhất
2. Genre (28%) - Thể loại game
3. Publisher (25%) - Nhà phát hành
4. Platform (12%) - Nền tảng

## Tài liệu tham khảo

1. Gregory Smith. (2016). *Video Game Sales Dataset*. Kaggle.
2. VGChartz - Video Game Charts and Sales Data
3. Wes McKinney. (2022). *Python for Data Analysis* (3rd Edition)
4. Jake VanderPlas. (2016). *Python Data Science Handbook*
5. Aurélien Géron. (2022). *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow*

## 📝 License

Dataset được sử dụng cho mục đích học tập và nghiên cứu theo điều khoản của Kaggle.

---
*Đồ án môn Lập Trình Cho Khoa Học Dữ Liệu (Programming for Data Science)*  
*Trường Đại học Khoa học Tự nhiên, ĐHQG-HCM*
