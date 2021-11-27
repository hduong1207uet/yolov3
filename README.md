# yolov3
# Train Yolov3 sử dụng COCO Dataset
1. Clone project và cài gói Poetry để quản lý Dependency trong Python
```
git clone https://github.com/hduong1207uet/yolov3
cd yolov3
pip3 install poetry --user
poetry install
```

Chúng ta cần tham gia môi trường ảo bằng cách chạy ```poetry shell``` trong thư mục này trước khi chạy bất kỳ lệnh nào sau đây mà không có tiền tố ```poetry run```.

2. Tải xuống các file **weights** đã được huấn luyện trước
```./weights/download_weights.sh```
  
3. Tải xuống COCO dataset
```./data/get_coco_dataset.sh```
  
4. Để đào tạo về COCO bằng cách sử dụng phụ trợ Darknet-53 được đào tạo trước trên ImageNet chạy

```poetry run yolo-train --data config/coco.data  --pretrained_weights weights/darknet53.conv.74```
