# 导出适配rknn的模型

该仓库只用在导出适配rknn的模型，参考yolov8的修改：https://github.com/airockchip/ultralytics_yolov8/blob/main/RKOPT_README.zh-CN.md

## 导出适配的onnx模型

```
# 修改 ./ultralytics/cfg/default.yaml 中 model 文件路径，默认为 yolov10n.pt，若自己训练模型，请调接至对应的路径。

pip install -r requirements.txt

export PYTHONPATH=./
python ./ultralytics/engine/exporter.py

# 执行完毕后，会生成 ONNX 模型，如果是yolov10n.pt，会在同级目录下生成yolov10n.onnx模型文件。
```

## 模型转换和简单部署

RKNN Toolkit Lite2简单部署测试参考： https://doc.embedfire.com/linux/rk356x/Python/zh/latest/ai/yolov10.html

# 参考链接

https://github.com/kaylorchen/rk3588-yolo-demo

https://github.com/airockchip/ultralytics_yolov8
