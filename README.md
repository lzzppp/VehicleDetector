# VehicleDetector
A code that is easy to detect vehicles based on yolo

## Dataset
VehicleDataset: 链接: https://pan.baidu.com/s/1Zns9jL58hd16A2VMiSA0KA 提取码: r97j

## installation

## Pipline
### Finetune from Just Vehicle Dataset from Coco weight

···
  python train.py --data VehicleFamily.yaml --epochs 300 --weights yolovx.pt --cfg yolov5x.yaml  --batch-size 32
···

### Finetune2 from custom dataset

···
  python train.py --data custom.yaml --epochs 300 --weights yolovxv.pt --cfg yolov5x.yaml  --batch-size 32
···

### Large model distillation to small model

···
  python train_distill.py --data VehicleFamily.yaml --epochs 300 --weights yolovmv.pt --teacher_weights yolovxv.pt --cfg yolov5x.yaml  --batch-size 32
···
