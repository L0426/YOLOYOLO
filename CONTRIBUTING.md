# 贡献指南 Contributing Guide

感谢您对YOLOYOLO学习库的关注！我们欢迎所有形式的贡献。

Thank you for your interest in the YOLOYOLO learning repository! We welcome all forms of contributions.

## 如何贡献 How to Contribute

### 1. 报告问题 Report Issues
如果您发现任何问题或有建议，请创建一个Issue。

If you find any issues or have suggestions, please create an Issue.

### 2. 提交资料 Submit Materials

#### 论文 Papers
- 添加YOLO相关的学术论文链接
- 提供论文摘要和关键点
- 包含中英文说明

#### 教程 Tutorials
- 分享学习笔记和经验
- 提供代码示例
- 详细的步骤说明

#### 实现代码 Implementation Code
- 分享YOLO实现代码
- 提供使用说明
- 包含依赖项列表

#### 数据集 Datasets
- 分享数据集信息和链接
- 说明数据集的特点和用途
- 提供数据格式说明

### 3. 改进文档 Improve Documentation
- 修正错误
- 补充内容
- 改进格式

## 贡献流程 Contribution Process

1. **Fork仓库**
   ```bash
   # Fork this repository on GitHub
   ```

2. **创建分支**
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **进行修改**
   - 添加内容
   - 遵循现有格式
   - 保持中英文双语

4. **提交更改**
   ```bash
   git add .
   git commit -m "Add: 描述你的修改"
   git push origin feature/your-feature-name
   ```

5. **创建Pull Request**
   - 描述你的更改
   - 说明添加的内容
   - 等待审核

## 内容规范 Content Guidelines

### 文件命名 File Naming
- 使用有意义的文件名
- 使用小写字母和连字符
- 示例：`yolov8-tutorial.md`

### 格式要求 Format Requirements
- 使用Markdown格式
- 保持中英文双语
- 代码块使用语法高亮
- 包含适当的标题层级

### 质量标准 Quality Standards
- 内容准确可靠
- 格式清晰整洁
- 示例可运行
- 链接有效

## 代码示例规范 Code Example Standards

```python
# 好的示例：清晰、有注释
from ultralytics import YOLO

# 加载预训练模型
model = YOLO('yolov8n.pt')

# 在图像上进行预测
results = model('image.jpg')

# 显示结果
results[0].show()
```

## 行为准则 Code of Conduct

- 尊重他人
- 建设性反馈
- 友好交流
- 共同学习

## 问题 Questions

如有任何问题，欢迎创建Issue讨论。

If you have any questions, feel free to create an Issue for discussion.

## 致谢 Acknowledgments

感谢所有贡献者的付出！

Thanks to all contributors for their efforts!
