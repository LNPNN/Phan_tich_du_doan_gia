## Mục lục
- [Phân tích và dự đoán giá Laptop](https://github.com/LNPNN/Phan_tich_du_doan_gia?tab=readme-ov-file#ph%C3%A2n-t%C3%ADch-v%C3%A0-d%E1%BB%B1-%C4%91o%C3%A1n-gi%C3%A1-laptop)
- [Quy trình phân tíhc dữ liệu](https://github.com/LNPNN/Phan_tich_du_doan_gia/edit/main/README.md#quy-tr%C3%ACnh-ph%C3%A2n-t%C3%ADch)
- [Bộ dữ liệu](https://github.com/LNPNN/Phan_tich_du_doan_gia?tab=readme-ov-file#b%E1%BB%99-d%E1%BB%AF-li%E1%BB%87u)
- [Thư viện](https://github.com/LNPNN/Phan_tich_du_doan_gia?tab=readme-ov-file#th%C6%B0-vi%E1%BB%87n)
- [Mô hình dự đoán](https://github.com/LNPNN/Phan_tich_du_doan_gia?tab=readme-ov-file#m%C3%B4-h%C3%ACnh-d%E1%BB%B1-%C4%91o%C3%A1n)
# Phân tích và dự đoán giá Laptop
- Dự đoán giá laptop trên trang Chợ Tốt là nghiên cứu trong lĩnh vực phân tích dữ liệu, hướng tới việc áp dụng các kỹ thuật phân tích và xử lý dữ liệu để phân tích các yếu tố có thể gây ảnh hưởng đến giá cả, từ đó có thể đưa ra được các dự đoán về giá của các loại laptop. 
- Mục tiêu chính là thực hiện phân tích dữ liệu một cách chi tiết để hiểu rõ về các yếu tố ảnh hưởng đến giá cả laptop trên trang Chợ Tốt. Bằng cách sử dụng các kỹ thuật phân tích dữ liệu, thư viện và các công cụ như: Requests và BeautifulSoup để crawl dữ liệu; Plotly, Dash, Seaborn và Matplotlib để trực quan hóa dữ liệu một cách dễ nhìn và dễ hiểu, … Bên cạnh đó sử dụng thuật toán trong mô hình máy học như Xgboost, KNN, Decision Tree Regressor, Random Forest Regressor để dự đoán giá cả laptop.
# Quy trình phân tích:
- Tiền xử lý dữ liệu
Dữ liệu sau khi thu thập sẽ chứa những biến bị khuyết và ‘Đang cập nhật’. Để rút ngắn thời gian và cho ra kết quả chính xác hơn thì nhóm sẽ tiến hành xóa các dòng chứa các biến bị khuyết và ‘Đang cập nhật’. Sau khi xử lý thì bộ dữ liệu sẽ có số lượng khoảng 900 dòng dữ liệu.
- Phân tích dữ liệu
Phân tích các biến liên quan: xem xét sự ảnh hưởng của các biến đối với giá cả laptop, sử dụng các biểu đồ boxplot để so sánh giá giữa các biến.
Phân tích tương quan dữ liệu: vẽ ma trận tương quan, biểu đồ heatmap để xem xét mức độ ảnh hưởng giữa các biến dữ liệu.
Phân tích yếu tố giá trị gia tăng: sự tăng giảm của giá đối với từng biến giá trị.
Phân loại giá: phân loại giá thành các phân khúc thấp, trung bình, cao để có cái nhìn tổng quan về thị trường.
- Thực nghiệm mô hình:
Các phương pháp, thuật đã đã sử dụng để dự đoán giá Laptop bao gồm:
Phương pháp TfidfVectorizer: dùng để chuyển đổi văn bản thành các vector TF-IDF để có thể áp dụng vào các mô hình học máy.
Phương pháp train_test_split: được sử dụng để chia dữ liệu thành hai phần gồm tập train và tập test. Tập train được sử dụng để huấn luyện mô hình, trong khi tập test được sử dụng để đánh giá hiệu suất của mô hình.
Độ chính xác (R^2): là một độ đô đánh giá sự khớp của mô hình hồi quy với dữ liệu. Độ chính xác của mô hình có giá trị càng gần 1 thì mô hình khớp tốt hơn với dữ liệu. 
Các thuật toán máy học: Random Forest Regressor, Xgboost, K-Neighbors Regressor, Decision Tree Regressor là một số thuật toán đã được sử dụng để huấn luyện mô hình. Từ đó chọn ra mô hình cho kết quả huấn luyện tốt nhất.
- Đánh giá kết quả:
Sau khi phân tích và xây dựng mô hình dự đoán dựa trên dữ liệu giá, nhóm sẽ dựa vào những kiến thức đã học để đưa ra những kết luận về các biến gần mức đối xứng, mất đối xứng, những ảnh hưởng của các biến đối với giá cả, kết luận được các hãng, loại máy,... được bán ra với số lượng như thế nào và đưa ra lựa chọn mô hình huấn luyện dự trên kết quả huấn luyện.
![image](https://github.com/user-attachments/assets/131c8c55-8c53-49d0-950e-ab850bba7ec2)

# Bộ dữ liệu
Bộ dữ liệu về giá cả laptop, cung cấp thông tin chi tiết về các đặc điểm kĩ thuật và thuộc tính của từng loại sản phẩm gây ảnh hưởng trực tiếp tới giá cả. Bộ dữ liệu chứa các thông tin đa dạng về các yếu tố quan trọng như: tên máy, hãng sản xuất, dòng sản phẩm, tình trạng hiện tại, kích cỡ màn hình, chính sách bảo hành, bộ vi xử lý, dung lượng RAM, loại và dung lượng ổ cứng, xuất xứ, card đồ họa và giá cả tương ứng.
[Bộ dữ liệu](https://drive.google.com/drive/folders/1erbISKeFVsviivvYiiWvlA1qq17gapEs)
# Thư viện
- pandas
- numpy
- seaborn
- matplotlib
- dash
- statsmodels
# Mô hình dự đoán
- XGboost
- K-Neighbors Regressor
- Decision Tree Regressor
- Random Forest Regressor
