# PCB Defect Detection / Обнаружение дефектов печатных плат

---

## English

### Project Description
This repository presents an experimental study on automated defect detection in printed circuit boards (PCBs) using modern YOLO architectures (v8n, v8s, v8m) and RT‑DETR‑l.  
The project includes a complete pipeline: data loading and conversion to YOLO format, model training, metric calculation, visualization, and comparative analysis.

### Abstract
A comparative study of **YOLOv8n**, **YOLOv8s**, **YOLOv8m**, and **RT‑DETR‑l** architectures is conducted for automated PCB surface defect detection.  
The **DeepPCB** dataset (693 images, 6 defect classes) is used for training.  
Experimental results show:
- **YOLOv8m** achieves the best **mAP@0.5 = 0.957**.
- **RT‑DETR‑l** outperforms others in **mAP@0.5:0.95 = 0.561**.
- **YOLOv8s** is recommended for industrial applications as the optimal trade‑off between accuracy, speed, and model size.

### Key Results
| Model     | mAP@0.5 | mAP@0.5:0.95 | Precision | Recall | Size (MB) | ms/img |
|-----------|---------|--------------|-----------|--------|-----------|--------|
| yolov8m   | **0.9566**  | 0.5571       | 0.9774    | **0.9240** | 49.6      | 39.4   |
| rtdetr_l  | 0.9529      | **0.5613**   | **0.9799**| 0.9104 | 63.2      | 80.4   |
| yolov8s   | 0.9436      | 0.5442       | 0.9656    | 0.9047 | 21.5      | **36.5**   |
| yolov8n   | 0.9118      | 0.5226       | 0.9634    | 0.8369 | **6.0**       | 40.0   |

### How to Reproduce
1. Clone the repository:  
   `git clone https://github.com/kvadratI4/PCB-Defect-Detection.git`
2. Install dependencies:  
   `pip install `ultralytics`, `pandas`, `matplotlib`, `seaborn`
3. Run `pcb_defect_detection.ipynb` in Jupyter Lab/Notebook
4. Download data (link available on the top oj Jupyter File)
5. All results (plots, tables, models) will be generated automatically.

---

## Русский язык

### Описание проекта
Данный репозиторий содержит экспериментальное исследование по автоматизированному обнаружению дефектов на печатных платах с использованием архитектур YOLO (v8n, v8s, v8m) и RT‑DETR‑l.  
Проект включает полный пайплайн: загрузку и преобразование данных в формат YOLO, обучение моделей, расчёт метрик, визуализацию результатов и сравнительный анализ.

### Аннотация
В работе проводится сравнительное исследование архитектур **YOLOv8n**, **YOLOv8s**, **YOLOv8m** и **RT‑DETR‑l** для задачи автоматизированного обнаружения дефектов поверхности печатных плат.  
Для обучения использован датасет **DeepPCB** (693 изображения, 6 классов дефектов).  
Экспериментально показано, что:
- **YOLOv8m** достигает наилучшего **mAP@0.5 = 0.957**.
- **RT‑DETR‑l** превосходит по **mAP@0.5:0.95 = 0.561**.
- **YOLOv8s** рекомендуется для промышленного применения как оптимальный по соотношению точности, скорости и компактности.

### Ключевые результаты
| Model     | mAP@0.5 | mAP@0.5:0.95 | Precision | Recall | Size (MB) | ms/img |
|-----------|---------|--------------|-----------|--------|-----------|--------|
| yolov8m   | **0.9566**  | 0.5571       | 0.9774    | **0.9240** | 49.6      | 39.4   |
| rtdetr_l  | 0.9529      | **0.5613**   | **0.9799**| 0.9104 | 63.2      | 80.4   |
| yolov8s   | 0.9436      | 0.5442       | 0.9656    | 0.9047 | 21.5      | **36.5**   |
| yolov8n   | 0.9118      | 0.5226       | 0.9634    | 0.8369 | **6.0**       | 40.0   |

### Как воспроизвести
1. Клонируйте репозиторий:  
   `git clone https://github.com/kvadratI4/PCB-Defect-Detection.git`
2. Установите зависимости:  
   `pip install `ultralytics`, `pandas`, `matplotlib`, `seaborn`
3. Запустите `pcb_defect_detection.ipynb` в Jupyter Lab/Notebook
4. Скачайте данные (ссылка доступна сверху Jupyter файла)
5. Все результаты (графики, таблицы, модели) сгенерируются автоматически.