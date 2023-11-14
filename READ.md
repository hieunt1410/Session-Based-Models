## Data raw là 1 file csv với header lần lượt là ‘sessionId’, ‘timestamp’, ‘itemId’, ‘category’.
+ ‘sessionId’, ‘itemId’, ‘category’: '<int>'
+ ‘Timestamp’: <datetime: %Y-%m-%dT%H:%M:%SZ>. Ví dụ: 2023-11-14T10:20:00Z
Default Config

## Cách xử lý data TRON:
1. Lọc hết các session mà có tương tác với item < 2
2. Lọc hết các item mà có tương tác < 5 trong từng session
3. Data được chia ra 2 tập train, test. Train lấy các session phía trước của thời gian item đầu tiên trong session cuối cùng được tương tác - 1 ngày. Test lấy các session sau thời gian đó.
