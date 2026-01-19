# YOLO实现 Implementations

本目录存放YOLO的各种实现代码和示例。

This directory contains various YOLO implementations and examples.

## 官方实现 Official Implementations

### YOLOv5
- **仓库 Repository**: https://github.com/ultralytics/yolov5
- **框架 Framework**: PyTorch
- **特点 Features**: 易用、文档完善、社区活跃

### YOLOv8
- **仓库 Repository**: https://github.com/ultralytics/ultralytics
- **框架 Framework**: PyTorch
- **特点 Features**: 最新API、多任务支持

### YOLOv7
- **仓库 Repository**: https://github.com/WongKinYiu/yolov7
- **框架 Framework**: PyTorch
- **特点 Features**: 高精度、实时性能

### YOLOv4
- **仓库 Repository**: https://github.com/AlexeyAB/darknet
- **框架 Framework**: Darknet/C
- **特点 Features**: 原始实现、高效

## 第三方实现 Third-party Implementations

### PyTorch实现
- MMDetection中的YOLO
- Detectron2集成

### TensorFlow实现
- TensorFlow 2.x版本
- TensorFlow Lite移动端部署

### ONNX实现
- 跨平台推理
- 模型转换工具

## 代码示例 Code Examples

### 基础推理 Basic Inference
```python
# 示例：使用YOLOv8进行推理
from ultralytics import YOLO

model = YOLO('yolov8n.pt')
results = model('image.jpg')
```

### 模型训练 Model Training
```python
# 示例：训练自定义模型
from ultralytics import YOLO

model = YOLO('yolov8n.yaml')
model.train(data='custom.yaml', epochs=100)
```

## 实现对比 Implementation Comparison

| 版本 Version | 框架 Framework | 速度 Speed | 精度 Accuracy | 易用性 Ease of Use |
|-------------|---------------|-----------|--------------|-------------------|
| YOLOv5      | PyTorch       | 快 Fast   | 高 High      | 易 Easy           |
| YOLOv8      | PyTorch       | 快 Fast   | 高 High      | 易 Easy           |
| YOLOv7      | PyTorch       | 很快 Very Fast | 很高 Very High | 中 Medium    |
| YOLOv4      | Darknet       | 快 Fast   | 高 High      | 难 Hard           |
