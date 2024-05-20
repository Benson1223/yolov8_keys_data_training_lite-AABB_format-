[環境設定] 安裝Pytorch
-> conda install pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia

==================================================

[1] 安裝 Ultralytics YOLO：
-> pip install -U ultralytics

[2] 建立一個新模型：
-> python -c "from ultralytics import YOLO; model = YOLO('yolov8n.yaml')"

[3] 加載一個預訓練模型（推薦用於訓練）：
-> python -c "from ultralytics import YOLO; model = YOLO('yolov8n.pt')"

[4] 從 YAML 建立一個新模型並傳遞預訓練的權重：
-> python -c "from ultralytics import YOLO; model = YOLO('yolov8n.yaml').load('yolov8n.pt')"

[5] 訓練模型：
-> python -c "from ultralytics import YOLO; model = YOLO('yolov8n.yaml'); results = model.train(data='coco128.yaml', epochs=100, imgsz=640)"