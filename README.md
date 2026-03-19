# Link Youtube
# CÀI ĐẶT MÔI TRƯỜNG

## Bước 1 :Cài Python

    - Tải Python ≥ 3.8: Python.org

    - Khi cài, tích Add Python to PATH

## Bước 2 : Tạo môi trường ảo
    - tạo môi trường ảo : python -m venv animal_env

    - kích hoạt môi trường 
    
       + Windows: animal_env\Scripts\activate
       
## Bước 3 : Cài thư viện cần thiết

pip install tensorflow numpy pillow streamlit

# HUẤN LUYỆN MÔ HÌNH

## Bước 1 : Chuẩn bị dataset

    - Sử dụng dataset CIFAR-10 có sẵn.

    - Chỉ chọn ba lớp động vật: Bird, Cat, Dog.

    - Chuẩn hóa ảnh: chuyển giá trị pixel về khoảng từ 0 đến 1 để mô hình học tốt hơn.

    - Chuyển nhãn của ba lớp về 0, 1, 2 để phù hợp với mô hình.

    <img width="687" height="445" alt="image" src="https://github.com/user-attachments/assets/8784daf9-4d2d-40f3-b695-4faa1e030fea" />


## Bước 2 : 
    - Tạo mô hình CNN cơ bản gồm:

      + Lớp convolution để trích xuất đặc trưng từ ảnh.

      + Lớp pooling để giảm kích thước và giữ thông tin quan trọng.

      + Lớp flatten để chuyển dữ liệu 2D thành 1D.

      + Lớp dense để phân loại ảnh thành 3 lớp.

    - Chọn hàm mất mát sparse categorical crossentropy và thuật toán tối ưu Adam.

    <img width="715" height="458" alt="image" src="https://github.com/user-attachments/assets/3b095dab-a78b-404b-9293-666d1d50ff5b" />

## Bước 3: Huấn luyên mô hình

    - Chạy huấn luyện mô hình với dữ liệu đã chuẩn bị.

     - Chia dữ liệu thành dữ liệu huấn luyện và dữ liệu kiểm tra để theo dõi độ chính xác trong quá trình học.

     - Số vòng lặp huấn luyện (epochs) có thể là 10 hoặc nhiều hơn nếu muốn tăng độ chính xác.

 <img width="598" height="116" alt="image" src="https://github.com/user-attachments/assets/be134bef-6b1a-4a67-b816-0fbacff9c008" />

## Bước 4 : Lưu mô hình

    - Sau khi huấn luyện xong, lưu mô hình vào file .h5.

    - File này sẽ được dùng để dự đoán trên web mà không cần huấn luyện lại.

    <img width="397" height="133" alt="image" src="https://github.com/user-attachments/assets/81c677f7-7235-4990-bdbd-bd931e0f73f9" />

# CÀI ĐẶT VÀ CHẠY CHƯƠNG TRÌNH WEB

## Bước 1 : Tạo file app.py

## Bước 2 : Dán code Streamlit vào

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/5ed09c4e-e5be-49ab-ba30-2d1331cf7801" />


## Bước 3 : Đặt model vào cùng thư mục

<img width="447" height="127" alt="image" src="https://github.com/user-attachments/assets/c5a118d7-5da2-4ce2-9d07-c3e3de1e3d01" />

## Bước 4 : Chạy Web

##link youtobe:https://www.youtube.com/watch?v=ybD5VXUvkK8&t=7s
    - Mở terminal tại thư mục project: streamlit run app.py
    
    - Streamlit sẽ tự mở trình duyệt: http://localhost:8501

    - Tại đây bạn có thể tải ảnh lên và dự đoán.
