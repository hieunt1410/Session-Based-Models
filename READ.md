## Data raw là 1 file csv với header lần lượt là ‘sessionId’, ‘timestamp’, ‘itemId’, ‘category’.
+ ‘sessionId’, ‘itemId’, ‘category’: 'int'
+ ‘Timestamp’: %Y-%m-%dT%H:%M:%SZ. Ví dụ: 2023-11-14T10:20:00Z
### Tập Yoochoose
+ Train: toàn bộ các Session trước ngày mà Session cuối cùng được ghi nhận.
+ Test: toàn bộ các Session cùng ngày mà Session cuối cùng được ghi nhận.
### Tập Diginetica
+ Train: toàn bộ các Session trước tuần mà Session cuối cùng được ghi nhận.
+ Test: toàn bộ các Session cùng tuần mà Session cuối cùng được ghi nhận.
### Metrics
+ Recall, MRR Top k = 20
