## Data raw là 1 file csv với header lần lượt là ‘sessionId’, ‘timestamp’, ‘itemId’, ‘category’.
+ ‘sessionId’, ‘itemId’, ‘category’: 'int'
+ ‘Timestamp’: %Y-%m-%dT%H:%M:%SZ. Ví dụ: 2023-11-14T10:20:00Z

## Cách xử lý data TRON:
1. Lọc hết các session mà có tương tác với item < 2
2. Lọc hết các item mà có tương tác < 5 trong từng session
3. Data được chia ra 2 tập train, test. Train lấy các session phía trước của thời gian item đầu tiên trong session cuối cùng được tương tác - 1 ngày. Test lấy các session sau thời gian đó.

## Cách chạy model
1. Clone repo
   ```bash
   !git clone -b trans4rec https://github.com/UwU-tao/Session-Based-Models.git
   ```
2. Cài đặt requirements.
   ```bash
   cd Session-Based-Models/
  !pip install -r requirements.txt
  ```
3. Chuyển data vào project
  ```bash
  !mkdir datasets
  !mkdir datasets/yoochoose
  ```
Sau đó, ta sẽ chuyển file data dạng .csv hoặc .dat vào folder yoochoose, lưu ý rename file data thành yoochoose.csv hoặc yoochoose.dat
4. Tiền xử lý dữ liệu
  ```bash
  !python src/preprocessing.py --dataset 'yoochoose'
  ```
5. Chạy mô hình
   ```bash
   !python -m src --config-filename tron/yoochoose
   ```
