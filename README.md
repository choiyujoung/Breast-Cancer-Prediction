# 🩺 Machine Learning-based Breast Cancer Diagnosis Prediction
(머신러닝 기반 유방암 진단 예측 모델)

## 📌 Project Overview
본 프로젝트는 Scikit-learn의 유방 종양 데이터(`load_breast_cancer`)를 활용하여 악성(Malignant) 및 양성(Benign) 종양을 분류하는 머신러닝 예측 모델입니다. 의사결정나무(Decision Tree) 알고리즘을 활용하여 데이터를 분류하고, 시각화를 통해 모델의 분류 기준(의사결정 과정)을 직관적으로 해석하는 데 중점을 두었습니다.

## 🛠 Tech Stack
- **Language:** Python
- **Libraries:** Pandas, Scikit-learn, Matplotlib, Graphviz, Joblib

## 💡 Key Features & Workflow
1. **Data Preprocessing:** - `sklearn.datasets`의 원본 데이터를 Pandas DataFrame으로 변환하여 데이터 조작의 편의성을 높임.
   - 종양의 특징(Features)을 X로, 악성/양성 여부(Target/Label)를 y로 명확히 분리하여 1차원 벡터와 2차원 배열 형태에 대한 이해도 확립.
2. **Model Training:** `train_test_split`을 활용하여 데이터를 8:2 비율(`test_size=0.2`)로 분할한 뒤, `DecisionTreeClassifier` 학습 진행.
3. **Model Evaluation:** `accuracy_score` 지표를 활용하여 테스트 데이터에 대한 모델 성능 검증.
4. **Interpretability & Visualization:** - `tree.export_graphviz` 및 `matplotlib`의 `tree.plot_tree`를 사용하여 의사결정나무의 분류 기준(설계도)을 직관적인 그래프로 시각화.
5. **Model Serialization:** 학습이 완료된 모델을 `joblib.dump`를 이용해 `.joblib` 파일로 저장하여 재사용성 확보.

## 📊 Results
- **Accuracy (정확도):** **94.73%** 달성
- 모델 분류 시각화 결과:



<img width="2319" height="1212" alt="breast-cancer" src="https://github.com/user-attachments/assets/98d13fa9-4e7c-43de-8cd6-8629b98384cd" />
