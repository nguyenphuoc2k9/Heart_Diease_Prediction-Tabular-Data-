Giới thiệu
----------

Ensemble learning là một nhánh của machine learning trong đó thay vì cải thiện thuật toán của mô hình, ta kết hợp các mô hình lại và tổng hợp kết quả lại thông qua một aggregator. Ensemble learning gồm 3 kĩ thuật chính:

 - Bagging: thực hiện nhiều phiên bản model hình trên cùng một tập dữ liệu rồi tổng hợp kết quả dự đoán của mô hình bằng majority voting(tổng hợp kết quả bằng số đông). tiêu biểu : RandomForest
 - Boosting: xây dựng một phiên bản của mô hình rồi cải tiến dần để mô hình sau học được residual của mô hình trước. Tiêu biểu có thể kể đến 2 mô hình chính : AdaBoosting, GradientBoostingRegression
 - + AdaBoosting: sau khi xây dựng decision tree đầu tiên, mô hình sẽ thực hiện dự đoán trên dataset, các trọng số của mỗi sample sẽ được cập nhật lại thông qua mỗi lần dự đoán(giảm trọng số các sample dự đoán đúng, tăng trọng số các sample dự đoán sai)
 - + GradientBoostingRegression: kết quả dự đoán bắt đầu bằng giá trị trung bình của dataset, tính toán residual(error) của dự đoán đầu tiên, tiếp theo xây dựng cây dự đoán residual của cây trước đó. Để kiểm soát tốc độ học của mô hình, tránh overfitting bằng công thức  $\ Output = T +a*\sum R_i$
 - Stacking: sử dụng nhiêu mô hình machine learning cùng  một lúc để tạo nên một tập training dataset mới, sau đó dùng một mô hình mới gọi là meta model để train model trên tập dữ liệu mới.

 

Mục tiêu của Dự án
------------------

Dự án này được thiết kế như một bài tổng hợp nội dung của Module 3 khóa AIO, đồng thời xét ứng dụng của nó trên tập dataset `Cleveland.csv` về dự đoán bệnh tim.



Cấu trúc Dự án
--------------

Dự án bao gồm các thư mục và tệp tin chính như sau:
-   `data/`: Thư mục lưu trữ các cặp ảnh stereo đầu vào.-   `README.md`: Tệp tài liệu này.
-   `requirements.txt`: Danh sách các thư viện Python cần thiết.

Phụ thuộc
---------

Dự án này yêu cầu các thư viện Python sau:

-   `scikit-learn`: Thư viện giúp việc sử dụng các model và metric nhanh chóng và tiện lợi hơn
-   `numpy`: Thư viện NumPy cho tính toán số học.
- `Pandas`: Thư viện xử lý tabular data
- `matplotlib,Seaborn`: Thư viện để Visualize kết quả 

Cài đặt các thư viện này bằng lệnh sau:

bash

Copy code

`pip install -r requirements.txt`

Hướng dẫn Cài đặt
-----------------

1.  **Clone dự án từ GitHub**:

    bash

    Copy code
```
    git clone https://github.com/nguyenphuoc2k9/Heart_Diease_Prediction-Tabular-Data-
    
    cd Heart_Diease_Prediction-Tabular-Data-
```


2.  **Cài đặt các phụ thuộc**:

    bash

    `pip install requirements.txt`
3.  **Chạy lần lượt các code cell trong Jupiter Notebook**: Chạy từng cell code để xem performance của từng mô hình cụ thể trên bài toán dự đoán bệnh tim



Tài liệu Tham khảo
------------------

-   Bộ dự liệu Cleveland: [Tải về tại đây](https://drive.google.com/file/d/1HJOSH99mhgR7OasSy6dg21e_iTFpyljy/view?usp=drive_link)
