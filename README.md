# UDTGMT-lab01

## Mô hình 1: dựa trên bài hướng dẫn [1] của tác giả Pavan Sanagapati:

Conv2D ( size = 5, ReLU),
MaxPooling (size = 2),
Dropout (0.2),
Flatten,
Dense (32, activation = ‘ReLU’),
Dense(10, activation = 'softmax'),

Tổng số lượng tham số: 148,650.
Độ chính xác trên tập test (20% từ tập fashion-mnist_train): 91.89 %


## Mô hình 2: Dựa trên bài hướng dẫn [2] của tác giả Chinmay Rane.

Conv2D ( size = 3 , ReLU),
BatchNormalization,
Conv2D ( size = 3, ReLU),
BatchNormalization,
Dropout (0.25),
Conv2D ( size = 3, ReLU),
MaxPooling (size = 2),
Dropout (0.25),
Conv2D ( size = 3, ReLU),
BatchNormalization,
Dropout (0.25),
Flatten,
Dense (512, ReLU),
BatchNormalization,
Dropout (0.5),
Dense(128, ReLU),
BatchNormalization,
Dropout (0.5),
Dense(10, activation = 'softmax'),

Tổng số lượng tham số: 13,017,770.
Độ chính xác trên tập test (20% từ tập fashion-mnist_train): 94.05% 

## Mô hình 3: Tự xây dựa trên 2 mô hình trên

Conv2D ( size = 3 , ReLU),
Conv2D ( size = 3, ReLU),
MaxPooling (size = 2),
Dropout (0.2),
Conv2D ( size = 3, ReLU),
Conv2D ( size = 3, ReLU),
MaxPooling (size = 2),
Dropout (0.2),
Flatten,
Dense (512, ReLU),
BatchNormalization,
Dropout (0.5),
Dense(128, ReLU),
BatchNormalization,
Dropout (0.5),
Dense(10, activation = 'softmax'),

Tổng số lượng tham số: 659,306.
Độ chính xác trên tập test (20% từ tập fashion-mnist_train): 93.65%

Tài liệu tham khảo:

[1] https://www.kaggle.com/pavansanagapati/a-tutorial-cnn-model-fashion-mnist

[2] https://www.kaggle.com/fuzzywizard/fashion-mnist-cnn-keras-accuracy-93
