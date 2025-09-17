# CardioPath-Kaggle-IMA205: Cardiac Pathology Prediction from MRI Scans

This repository contains my solution to the **IMA205 Kaggle Challenge on Cardiac Pathology Prediction**.  
I developed a two-stage pipeline combining **U-Net–based segmentation** with **classical machine learning classification** to diagnose cardiac pathologies from CMRI exams.

---

## 📝 Project Overview
Accurate analysis of cardiac structure and function from MRI scans is critical for early detection of cardiovascular diseases.  
This project classifies patients into five diagnostic categories:

- Healthy controls  
- Myocardial infarction  
- Dilated cardiomyopathy  
- Hypertrophic cardiomyopathy  
- Abnormal right ventricle  

I used the provided CMRI dataset (150 subjects) split into training/validation and test sets. My approach consisted of:

1. **Segmentation:** Using U-Net to segment the left ventricle, right ventricle, and myocardium from CMRI images.  
2. **Feature Extraction:** Computing clinically relevant metrics such as ventricular volumes, ejection fractions, myocardial mass, and patient anthropometrics.  
3. **Classification:** Training Random Forest, AdaBoost, and SVM models on the extracted features to predict pathology classes.

---

## 🔍 Key Features
- **U-Net Segmentation:** Achieved Dice ≥ 0.96 and IoU ≥ 0.93 on validation data.  
- **Feature Engineering:** Extracted ejection fractions, ventricular volumes, myocardial mass, and patient BSA.  
- **Classification:** Random Forest delivered the best performance with **85% test accuracy on the Kaggle leaderboard**.  
- **Interpretability:** Analyzed feature importance to identify the strongest predictors (e.g., LV end-systole volume, LV ejection fraction).  

---

## 📊 Results
- **Segmentation Metrics:**  
  - LV Dice: 0.97 | IoU: 0.95  
  - RV Dice: 0.96 | IoU: 0.93  
  - MYO Dice: 0.97 | IoU: 0.90  
- **Classification:** 85% test accuracy on Kaggle leaderboard.  
- **Workflow:** Transparent and interpretable two-stage pipeline combining deep learning and classical ML.

---

## 🛠️ Tech Stack
- Python 3  
- PyTorch (U-Net implementation)  
- Scikit-learn (Random Forest, AdaBoost, SVM)  
- NumPy, Pandas, Matplotlib  
- Nibabel (for NIfTI image handling)

---

## 👩‍💻 Author
Developed individually by Luiz Fernando MOREIRA TEIXEIRA as part of the IMA205 Kaggle Challenge.

---

## 📄 Report
For full details on methodology, experiments, and results, please see the attached report (PDF).

---

## 📚 References
- [1] O. Ronneberger, P. Fischer, and T. Brox. “U-Net: Convolutional Networks for Biomedical Image Segmentation”. In: CoRR abs/1505.04597 (2015). [arXiv:1505.04597](http://arxiv.org/abs/1505.04597).  
- [2] M. Khened, V. Alex, and G. Krishnamurthi. “Densely Connected Fully Convolutional Network for Short-Axis Cardiac Cine MR Image Segmentation and Heart Diagnosis Using Random Forest”. In: *Statistical Atlases and Computational Models of the Heart. ACDC and MMWHS Challenges*. Ed. by M. Pop et al. Cham: Springer International Publishing, 2018, pp. 140–151. ISBN: 978-3-319-75541-0.  
- [3] J. M. Wolterink et al. “Automatic Segmentation and Disease Classification Using Cardiac Cine MR Images”. In: *Statistical Atlases and Computational Models of the Heart. ACDC and MMWHS Challenges*. Ed. by M. Pop et al. Cham: Springer International Publishing, 2018, pp. 101–110. ISBN: 978-3-319-75541-0.

