# Mr. Durian: Durian Image Classifier by CNN

โครงงานพัฒนาโมเดล Deep Learning (Convolutional Neural Networks) เพื่อจำแนกสายพันธุ์ทุเรียนยอดนิยมในประเทศไทย โดยใช้การวิเคราะห์รูปภาพเพื่อระบุลักษณะเฉพาะของแต่ละสายพันธุ์

## 📌 บทนำ (Introduction)
ทุเรียนเป็นผลไม้เศรษฐกิจที่สำคัญของไทย อย่างไรก็ตาม การแยกแยะสายพันธุ์จากลักษณะภายนอก (เช่น หนาม และรูปทรงผล) อาจทำได้ยากสำหรับผู้บริโภคทั่วไป โครงงานนี้จึงนำเทคนิค Image Classification มาประยุกต์ใช้เพื่อช่วยระบุสายพันธุ์ทุเรียนได้อย่างแม่นยำ

## 🛠️ วิธีการดำเนินงาน (Methodology)

### 1. ข้อมูลที่ใช้ (Dataset Description)
* **แหล่งที่มา:** Durian Trading Website, Facebook, และ YouTube (Video Capture)
* **Dataset :** https://drive.google.com/drive/folders/1mWZ18RnC0A8gISBpstNX71yurxO11wv0?usp=sharing
* **สายพันธุ์ที่ใช้ทดสอบ:**
    * ชะนี (Chanee)
    * ก้านยาว (Kanyao)
    * หลงลับแล (Longlubae)
    * หมอนทอง (Monthong)
* **การจัดการข้อมูล:** ใช้เทคนิค **Data Augmentation** (Resizing, Rescaling, Rotation, Zoom) เพื่อเพิ่มความหลากหลายของข้อมูลและป้องกัน Overfitting

### 2. โมเดลที่ใช้เปรียบเทียบ (Model Selection)
โครงงานนี้ได้ทำการเปรียบเทียบประสิทธิภาพของโมเดล Pre-trained ยอดนิยม 4 รูปแบบ:
1. **EfficientNetB7**
2. **InceptionV3**
3. **ResNet**
4. **MobileNetV2**

## 📊 ผลการทดสอบ (Results)
จากการทดสอบพบว่าการใช้เทคนิค **Fine-Tuning** ช่วยเพิ่มประสิทธิภาพของโมเดลได้อย่างมีนัยสำคัญ:

| Model | Accuracy (without Fine-Tuning) | Accuracy (with Fine-Tuning) |
| :--- | :---: | :---: |
| **EfficientNetB7** | 72.98% | **83.14%** |
| **InceptionV3** | 49.06% | 76.14% |
| **MobileNetV2** | 55.65% | 80.00% |
| **ResNet** | 36.18% | 53.26% |

**สรุปผล:** โมเดล **EfficientNetB7** ให้ค่าความแม่นยำสูงสุดที่ **83.14%** หลังจากการทำ Fine-Tuning

## 🚀 การนำไปใช้งาน (Future Work)
* พัฒนาโมเดลให้สามารถจำแนกทุเรียนแบบ "เฉพาะเนื้อ" (Durian Meat) ได้แม่นยำขึ้น
* ขยายขอบเขตการจำแนกไปยังสายพันธุ์พื้นเมืองอื่นๆ

## 📝 จัดทำโดย




## 📚 เครื่องมือที่ใช้ (Tools & Libraries)
* Python
* TensorFlow / Keras
* OpenCV
* Matplotlib / Seaborn

