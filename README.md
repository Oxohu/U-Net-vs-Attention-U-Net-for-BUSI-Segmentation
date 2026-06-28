👤 Name:

Nafisat Abdulsalam

📂 Project:

Breast Ultrasound Lesion Segmentation using U-Net and Attention U-Net

🫁 Organ / Body Part:

Breast (Breast Ultrasound Lesion Segmentation)

📦 Dataset Used:

Breast Ultrasound Images Dataset (BUSI)

* 780 breast ultrasound images
* 437 Benign
* 210 Malignant
* 133 Normal
* Images resized to 256 × 256 pixels
* Multiple lesion masks for a single image were merged into one binary ground truth mask before training.
* Dataset split: 80% Training and 20% Validation

🧠 Model / Method:

Models Compared:

* Standard U-Net
* Attention U-Net

Architecture Details:

* Encoder–Decoder Convolutional Neural Network with Skip Connections
* Attention Gates integrated into the decoder for Attention U-Net
* Input Size: 256 × 256 RGB images
* Loss Function: Dice Loss
* Optimizer: Adam (Learning Rate = 0.0001)
* Batch Size: 16
* Evaluation Metrics: Dice Coefficient, IoU, Binary Accuracy, Precision, and Recall

📊 Results:

U-Net(stopped after 9 epochs)

* Dice Score: 0.1254 (12.54%)
* IoU: ≈ 0.0000
* Loss: 0.8744
* Accuracy: 0.9234
* Precision: 0.0000
* Recall: 0.0000

Attention U-Net(completed 30 epochs)

* Dice Score: 0.6238 (62.38%)
* IoU: 0.5451 (54.51%)
* Loss: 0.3791
* Accuracy: 0.9560
* Precision: 0.7323
* Recall: 0.6701

The Attention U-Net significantly outperformed the standard U-Net, producing more accurate lesion segmentation masks and substantially improving Dice Score, IoU, Precision, and Recall.

🤔 Challenges Faced:
* Balancing computational efficiency and segmentation accuracy by resizing all images to 256 × 256.
* Maintaining identical preprocessing, training configuration, and evaluation metrics to ensure a fair comparison between the Standard U-Net and Attention U-Net.
