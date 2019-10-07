# UDTGMT-lab01

Mô hình 1: dựa trên bài hướng dẫn [1] của tác giả Pavan Sanagapati:

Conv2D ( size = 5, ReLU)

MaxPooling (size = 2)

Dropout (0.2)

Flatten

Dense (32, activation = ‘ReLU’)	

Dense(10, activation = 'softmax')

Tổng số lượng tham số: 148,650.

Độ chính xác trên tập test (20% từ tập fashion-mnist_train): 91.89 %

Mô hình 2: Dựa trên bài hướng dẫn [2] của tác giả Chinmay Rane.

Conv2D ( size = 3 , ReLU)

BatchNormalization

Conv2D ( size = 3, ReLU)

BatchNormalization

Dropout (0.25)

Conv2D ( size = 3, ReLU).

MaxPooling (size = 2)

Dropout (0.25)

Conv2D ( size = 3, ReLU)

BatchNormalization

Dropout (0.25)

Flatten

Dense (512, ReLU)

BatchNormalization

Dropout (0.5)

Dense(128, ReLU)

BatchNormalization

Dropout (0.5)

Dense(10, activation = 'softmax')

Tổng số lượng tham số: 13,017,770

Độ chính xác trên tập test (20% từ tập fashion-mnist_train): 94.05% 

•	Nhận xét: Mô hình phức tạp nhưng độ chính xác cao, dồng nghĩa thời gian huấn luyện lâu (khoảng 3h). Dù mô hình mạng CNN lấy từ bài hướng dẫn [2] nhưng mọi thao tác còn lại đều làm giống bài hướng dẫn [1]. Kết quả độ chính xác trong bài hướng dẫn [2] với 54,000 ảnh train và 6,000 ảnh test là 92.95% nhưng độ chính xác trong thử nghiệm này với 48,000 ảnh train và 12,000 ảnh test là 94.05%. 

Mô hình 3: Tự xây dựa trên 2 mô hình trên
Lớp (loại)	Output shape	Tham số
Conv2D ( size = 3 , ReLU)	(None, 26, 26, 32)	320
Conv2D ( size = 3, ReLU)	(None, 24, 24, 32)	9248
MaxPooling (size = 2)	(None, 12, 12, 32)	0
Dropout (0.2)	(None, 12, 12, 32)	0
Conv2D ( size = 3, ReLU)	(None, 10, 10, 64)	18496
Conv2D ( size = 3, ReLU)	(None, 8, 8, 64)	73856
MaxPooling (size = 2)	(None, 4, 4, 64)	0
Dropout (0.2)	(None, 14, 14, 128)	0
Flatten	(None, 25088)	0
Dense (512, ReLU)	(None, 512)	12845568
BatchNormalization	(None, 512)	2048
Dropout (0.5)	(None, 512)	0
Dense(128, ReLU)	(None, 128)	65664
BatchNormalization	(None, 128)	512
Dropout (0.5)	(None, 128)	0
Dense(10, activation = 'softmax')	(None, 10)	1290

Tổng số lượng tham số: 659,306
Độ chính xác trên tập test (20% từ tập fashion-mnist_train): 93.65%

Tài liệu tham khảo:
[1] https://www.kaggle.com/pavansanagapati/a-tutorial-cnn-model-fashion-mnist
[2] https://www.kaggle.com/fuzzywizard/fashion-mnist-cnn-keras-accuracy-93
