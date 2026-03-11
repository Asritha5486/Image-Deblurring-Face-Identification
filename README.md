# GAN-Based Image Deblurring and Face Identification

## Overview
This project presents a deep learning–based computer vision pipeline designed to restore blurred facial images and accurately identify individuals in surveillance scenarios. Motion blur caused by camera shake, subject movement, or poor lighting significantly affects face recognition systems. 

To address this challenge, the system integrates **GAN-based image restoration** with **deep metric learning–based face recognition** to improve identification accuracy from blurred surveillance images.

The proposed pipeline uses **DeblurGAN-v2** to restore blurred images, **MTCNN** for robust face detection and alignment, and **FaceNet** to extract discriminative facial embeddings for identity recognition.

---

## System Architecture

Pipeline:

Blurred Image  
→ Image Deblurring (DeblurGAN-v2)  
→ Face Detection (MTCNN)  
→ Face Alignment  
→ Feature Extraction (FaceNet)  
→ Embedding Matching (Cosine Similarity)  
→ Identity Prediction

---

## Key Features

- GAN-based motion blur removal using **DeblurGAN-v2**
- Robust face detection using **MTCNN**
- Deep metric learning with **FaceNet embeddings**
- Identity matching using **Cosine Similarity**
- Works on **synthetic blurred images and CCTV-style surveillance images**
- Improves recognition accuracy in degraded environments

---

## Technologies Used

- Python
- Deep Learning
- Generative Adversarial Networks (GANs)
- DeblurGAN-v2
- MTCNN
- FaceNet
- OpenCV
- PyTorch / TensorFlow
- NumPy
- Computer Vision

---

## Dataset

A custom **CCTV-style face dataset** was created by collecting clear facial images and applying:

- Motion Blur
- Gaussian Blur

to simulate real-world surveillance conditions such as:

- Camera shake
- Low lighting
- Subject movement

Images were preprocessed using:

- Resizing
- Normalization
- Histogram Equalization

---

## Performance Results

| Metric | Blurred | Deblurred |
|------|------|------|
| PSNR | 22.3 dB | 26.8 dB |
| SSIM | 0.79 | 0.91 |
| Face Detection Precision | 82% | 91% |
| Face Recognition Accuracy | 63% | 87% |

The results demonstrate that **image restoration significantly improves recognition accuracy**.

---

## Recognition Algorithm

1. Input blurred image
2. Restore image using DeblurGAN-v2
3. Detect faces using MTCNN
4. Align detected faces
5. Extract 128-D embeddings using FaceNet
6. Compare embeddings with database using cosine similarity
7. If similarity > threshold → Identity recognized  
8. Otherwise → Unknown

---

## Applications

- Surveillance systems
- CCTV security monitoring
- Law enforcement investigations
- Forensic video analysis
- Access control systems

---

## Future Work

- Improve performance under **extreme low-light conditions**
- Implement **real-time edge deployment**
- Integrate **domain adaptation for different surveillance environments**
- Explore lightweight GAN models for faster inference

---

## Author

**Asritha Chunduri**

Computer Science / AI Enthusiast  
Interested in **Computer Vision, Deep Learning, and Generative AI**

GitHub:  
https://github.com/Asritha5486

---

## License

This project is intended for **research and educational purposes**.
