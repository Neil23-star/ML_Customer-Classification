### ML_Customer-Classification (Phân loại khách hàng)
### 1. Description

   Homesite, nhà cung cấp hàng đầu về bảo hiểm nhà ở. Homesite muốn tìm ra với mức thu nhập và mức giá bảo hiểm như thế nào thì khách hàng sẽ mua bảo hiểm nhà ở của họ. Từ đó điều chỉnh mức giá niêm yết bảo hiểm phù hợp để gia tăng doanh số. Sử dụng cơ sở dữ liệu ẩn danh thông tin về khách hàng và hoạt động bán bảo hiểm của công ty, bao gồm thông tin về giá trị tài sản và mức giá bảo hiểm. Tập dữ liệu có thể được tìm thấy tại [đây](https://www.kaggle.com/c/homesite-quote-conversion).
  
  Sử dụng các thư viện và thuật toán trên thư viện Spark Machine Learning. 
### 2. Preprocessing data and EDA

   Kiểm tra xử lý các giá trị bị thiếu.
   
   Exploratory data analysis (EDA).
   
   Biến đổi sang định dạng Spark để tiến hành xây dựng model.
 ### 3. Modelling and Evaluation
 #### 3.1 Modelling
   Mô hình Logistic Regression: Sử dụng hàm logit để dự đoán xác suất.
   
   Mô hình Decision Tree: Tìm biến độc lập quan trọng nhất để tạo nhóm. Decision tree là tên đại diện cho một nhóm thuật
toán phát triển dựa trên decision tree. Ở đó, mỗi node của cây sẽ là các thuộc tính, và các nhánh là giá trị lựa
chọn của thuộc tính đó. Bằng cách đi theo các giá trị thuộc tính trên cây, decision tree sẽ cho ta biết giá trị dự
đoán.

   Mô hình Random Forest: Thuật toán này xây dựng nhiều cây quyết định và hợp nhất chúng lại với nhau.
 #### 3.2 Evaluation
   Gini: là tỷ số giữa đường cong $ROC$ và đường $diagnol line$ & diện tích của tam giác trên (the area of the above triangle). Vì vậy, chúng ta có thể tính toán $Gini$ theo công thức sau:

   $$Gini = 2*AUC - 1$$

   Trong đó, $AUC$ (Area Under the Curve) là diện tích nằm dưới $ROC$ curve. $ROC$ là một đường cong biểu diễn xác suất. Chỉ số $AUC$ càng gần 1 thì mô hình càng phân loại chính xác. $AUC$ càng gần 0.5 thì hiệu suất phân loại càng tệ còn nếu gần 0 thì mô hình sẽ phân loại ngược kết quả (phân loại dương tính thành âm tính và ngược lại). Ví dụ , $Gini$ đạt giá trị trên 0.6 thì  mô hình tốt.
   
   
