# HW2 – Long Tail Object Detection
**Student :** 清大 工工所 李家欣 113034506

**Environment:** Google Colab Pro (T4 GPU + High RAM)

---
## 1. 專案說明
本專案為 長尾分布空拍影像偵測任務，
主要結合 YOLOv8-P2（偵測小物體）與 RT-DETR-L（Transformer 架構）進行異構融合，
以提升少數類別（person、motorcycle）的偵測表現。


## 2. 環境設定
- 平台：Google Colab Pro

| Item | Specification |
|------|----------------|
| GPU | NVIDIA Tesla T4 (16 GB VRAM) |
| Runtime | High-RAM (~50 GB) |
| Python | 3.12 (default on Colab) |
| Framework | PyTorch 2.x (CUDA 12.x preinstalled) |

- Python：3.12
- CUDA：12.6
- PyTorch：2.4.0
- 執行前請確認：
  - 已登入 Google Colab
  - 已掛載 Google Drive
  - 已在 Drive 建立專案資料夾（例如：/content/drive/MyDrive/ComputerVision_DL/hw2_longtail_od/）


## 3. 資料結構
```bash
📦 hw2_longtail_od/
├── taica-cvpdl-2025-hw-2.zip # 資料集
├── ckpts/                    # 已訓練完成的 4 個模型權重
│   ├── best_f0.pt
│   ├── best_f1.pt
│   ├── best_f2.pt
│   └── best_rtdetr.pt
├── rtdetr_main.ipynb                # RT-DETR 推論與訓練主程式
├── yolov8p2.ipynb            # YOLOv8-P2 訓練 Notebook
├── requirements.txt 
└── submissions/     
  ```

## 4. 使用方式
1. 可以直接使用我已經從零訓練過的模型參數，跑rtdetr_main.ipynb 中，滾到最下方的 "推論 cell"去執行
2. 若想要重現模型訓練過程:
  - YOLOv8-P2 :依序執行yolov8p2.ipynb
  - RT-DETR-L :依序執行rtdetr_main.ipynb  
