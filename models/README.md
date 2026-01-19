# YOLO模型 Models

本目录存放预训练模型和模型权重信息。

This directory contains information about pre-trained models and model weights.

## 预训练模型 Pre-trained Models

### YOLOv8模型 YOLOv8 Models

| 模型 Model | 大小 Size | mAPval | 速度 Speed | 参数量 Params | FLOPs |
|-----------|----------|--------|-----------|--------------|-------|
| YOLOv8n   | 640      | 37.3   | 80ms      | 3.2M         | 8.7B  |
| YOLOv8s   | 640      | 44.9   | 128ms     | 11.2M        | 28.6B |
| YOLOv8m   | 640      | 50.2   | 234ms     | 25.9M        | 78.9B |
| YOLOv8l   | 640      | 52.9   | 375ms     | 43.7M        | 165.2B|
| YOLOv8x   | 640      | 53.9   | 479ms     | 68.2M        | 257.8B|

### YOLOv5模型 YOLOv5 Models

| 模型 Model | 大小 Size | mAPval | 速度 Speed | 参数量 Params | FLOPs |
|-----------|----------|--------|-----------|--------------|-------|
| YOLOv5n   | 640      | 28.0   | 6.3ms     | 1.9M         | 4.5B  |
| YOLOv5s   | 640      | 37.4   | 6.4ms     | 7.2M         | 16.5B |
| YOLOv5m   | 640      | 45.4   | 8.2ms     | 21.2M        | 49.0B |
| YOLOv5l   | 640      | 49.0   | 10.1ms    | 46.5M        | 109.1B|
| YOLOv5x   | 640      | 50.7   | 12.1ms    | 86.7M        | 205.7B|

## 模型下载 Model Download

### 官方权重 Official Weights
权重文件可以从以下官方发布页面下载，选择适合您需求的模型大小：

Weights can be downloaded from the following official release pages, select the model size that fits your needs:

- **YOLOv8**: https://github.com/ultralytics/assets/releases (下载 yolov8n.pt, yolov8s.pt 等)
- **YOLOv5**: https://github.com/ultralytics/yolov5/releases (下载 yolov5n.pt, yolov5s.pt 等)
- **YOLOv7**: https://github.com/WongKinYiu/yolov7/releases (下载 yolov7.pt, yolov7-tiny.pt 等)

### 使用方法 Usage
```python
from ultralytics import YOLO

# 自动下载预训练权重
model = YOLO('yolov8n.pt')

# 或加载本地权重
model = YOLO('path/to/weights.pt')
```

## 模型转换 Model Conversion

### PyTorch to ONNX
```python
model = YOLO('yolov8n.pt')
model.export(format='onnx')
```

### PyTorch to TensorRT
```python
model = YOLO('yolov8n.pt')
model.export(format='engine')
```

### PyTorch to CoreML
```python
model = YOLO('yolov8n.pt')
model.export(format='coreml')
```

## 模型选择指南 Model Selection Guide

### 根据应用场景 By Application

- **移动端部署 Mobile**: YOLOv8n, YOLOv5n
- **边缘设备 Edge**: YOLOv8s, YOLOv5s
- **服务器推理 Server**: YOLOv8m/l, YOLOv5m/l
- **高精度需求 High Accuracy**: YOLOv8x, YOLOv7

### 根据性能需求 By Performance

- **实时性优先 Real-time**: 选择较小模型（n/s）
- **精度优先 Accuracy**: 选择较大模型（l/x）
- **平衡性能 Balanced**: 选择中等模型（m）

## 微调模型 Fine-tuning

```python
# 加载预训练模型
model = YOLO('yolov8n.pt')

# 在自定义数据集上微调
model.train(
    data='custom.yaml',
    epochs=100,
    imgsz=640,
    batch=16
)
```
