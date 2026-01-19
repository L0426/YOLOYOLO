# YOLO数据集 Datasets

本目录存放YOLO训练和测试相关的数据集信息。

This directory contains information about datasets for YOLO training and testing.

## 常用数据集 Common Datasets

### COCO (Common Objects in Context)
- **类别数 Classes**: 80
- **图像数 Images**: 330K
- **用途 Usage**: 通用目标检测
- **链接 Link**: https://cocodataset.org/

### Pascal VOC
- **类别数 Classes**: 20
- **图像数 Images**: 20K
- **用途 Usage**: 目标检测和分割
- **链接 Link**: http://host.robots.ox.ac.uk/pascal/VOC/

### Open Images
- **类别数 Classes**: 600
- **图像数 Images**: 9M
- **用途 Usage**: 大规模目标检测
- **链接 Link**: https://storage.googleapis.com/openimages/web/index.html

### ImageNet
- **类别数 Classes**: 1000+
- **图像数 Images**: 14M
- **用途 Usage**: 分类和检测
- **链接 Link**: https://www.image-net.org/

## 数据集格式 Dataset Formats

### YOLO格式
```
images/
  train/
    image1.jpg
    image2.jpg
  val/
    image3.jpg
labels/
  train/
    image1.txt
    image2.txt
  val/
    image3.txt
```

### 标注格式 Annotation Format
```
<class_id> <x_center> <y_center> <width> <height>
```

## 数据集配置 Dataset Configuration

### 配置文件示例 Config Example (YAML)
```yaml
# dataset.yaml
path: ../datasets/custom
train: images/train
val: images/val
test: images/test

nc: 80  # number of classes
names: ['person', 'bicycle', 'car', ...]
```

## 数据准备 Data Preparation

1. **收集数据 Collect Data**
   - 采集图像
   - 确保数据多样性

2. **标注数据 Annotate Data**
   - 使用标注工具（LabelImg, CVAT等）
   - 标注目标边界框

3. **数据划分 Split Data**
   - 训练集：70-80%
   - 验证集：10-15%
   - 测试集：10-15%

4. **数据增强 Data Augmentation**
   - 翻转、旋转
   - 缩放、裁剪
   - 颜色变换

## 标注工具 Annotation Tools

- **LabelImg**: 简单易用的标注工具
- **CVAT**: 在线协作标注平台
- **Roboflow**: 数据集管理和增强
- **Labelbox**: 企业级标注平台
