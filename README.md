# yolov8

##### 2023.08.30 By:zttszfts@gmail.com

## 常用命令


单卡训练
<pre><code>yolo task=detect mode=train model=yolov8n.pt data=mark.yaml batch=32 epochs=100 imgsz=640 workers=0 device=0</code></pre>
模型验证
<pre><code>yolo task=detect mode=val model=runs/detect/train/weights/best.pt data=mark.yaml device=0</code></pre>
模型预测（调用摄像机）
<pre><code>yolo task=detect mode=predict model=runs/detect/train/weights/best.pt source=0 device=0</code></pre>
模型导出onnx
<pre><code>yolo task=detect mode=export model=runs/detect/train/weights/best.pt format=onnx</code></pre>
模型导出onnx（适用于unity老版本）
<pre><code>yolo task=detect mode=export model=runs/detect/train/weights/best.pt format=onnx opset=10</code></pre>