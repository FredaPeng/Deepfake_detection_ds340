# Deepfake_detection_ds340
DS 340 Machine Learning Final Project, training model for deepfake detection based on CNN, XceptionNet, EfficientNet
**README Notes:**  
- **Environment & Data Paths**  
  - Baseline notebooks (`Deepfake_detect_base1.ipynb`, `Deepfake_detect_base2.ipynb`) run on Colab; data is pulled via KaggleHub.  
  - `Deepfake_detect1.ipynb` & `Deepfake_detect2.ipynb` run on the SCC cluster. Set at top of each notebook:  
    ```python
    BASE_DIR = "/projectnb/ds340/projects/MS"
    ```  
- **References & Attribution**  
  - Li et al., “DeepFake Detection with EfficientNet,” *The Visual Computer* (2024). https://link.springer.com/article/10.1007/s00371-024-03690-y  
  - Bharadiya, J., “Cracking the Code: Unmasking DeepFakes with EfficientNet,” Medium (2024). https://jasminbharadiya.medium.com/cracking-the-code-unmasking-deepfakes-with-efficientnet-a-step-by-step-guide-7144dce4f4ed  
  - Keras EfficientNetV2 API docs: https://keras.io/api/applications/efficientnet_v2/  
  - Kaggle starter code: Daniel09817, “DeepFake Detection” (2023). https://www.kaggle.com/code/daniel09817/deepfake-detection  
- **How to Run**  
  1. Clone the repo.  
  2. Install dependencies:  
     ```bash
     pip install -r requirements.txt
     ```  
  3. **Colab (baseline)**: upload `kaggle.json`, then run the “Data Import” cells.  
  4. **SCC (detect1/2)**: verify `BASE_DIR` and ensure data is available under that path.
 
### 1. `Deepfake_detect1.ipynb`  
*(Exploration: model prep, augmentation experiments, hyperparameter sweeps — 25-epoch training)*

1. **Module import**  
2. **Data Preprocessing**  
3. **Data Augmentation Comparison**  
   - **CNN Baseline** 
   - **Horizontal Flip** 
   - **Rotation Augmentation**  
   - **Gaussian Noise** 
   - **JPEG Compression Artifacts** 
4. **Advanced Data Augmentation**  
5. **Data Augmentation**  
6. **Model Preparation – GPU**  
7. **Model Training (Epoch = 25)**  
   - **CNN** 
   - **XceptionNet**   
   - **EfficientNet**   
8. **Model Comparison: Best ⇒ EfficientNet**  
   - Epoch = 25  
9. **EfficientNet Hyperparameter Testing for Fine-tuning**  
10. **Hyperparameter tuning**  
11. **More Experiments**  
12. **Layer Unfreezing Function**  
13. **Learning Rate Schedule Functions**  
14. **Fine-Tuning Function** 
15. **Trial & Finding**  
16. **Key Findings from Your Experiments**  
    - Best-performing LR strategy  
    - Learning-rate importance  
    - Validation accuracy patterns  
    - Convergence speed observations  
17. **Grad_CAM**  

---

### 2. `Deepfake_detect2.ipynb`  
*(Refinement: focused retraining & fine-tuning — 50-epoch training)*

1. **Module import**  
2. **Data Preprocessing** 
3. **Data Augmentation Comparison**  
4. **Data Augmentation**  
5. **Model Preparation**  
6. **Model Training (Epoch = 50)**  
7. **EfficientNet Fine-tuning: Val_acc 89 % → 93 %**  

---

### 3. Baseline Notebooks  

- [Deepfake_detect_base1.ipynb](https://github.com/FredaPeng/Deepfake_detection_ds340/blob/main/Deepfake_detect_base1.ipynb)  
  - Baseline CNN, 10 epochs on original split  
- [Deepfake_detect_base2.ipynb](https://github.com/FredaPeng/Deepfake_detection_ds340/blob/main/Deepfake_detect_base2.ipynb)  
  - Baseline CNN, 20 epochs on original split  
