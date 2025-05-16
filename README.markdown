# AI-Powered Blood Disease Prediction Using Transfer Learning

This project utilizes transfer learning and AI to predict blood-related diseases using numerical blood test features, binary indicators, and blood smear image analysis. It provides disease predictions, mapped cell types, and personalized recommendations including treatments, a 7-day diet plan, precautions, and medical suggestions.

## Features

### 1. Disease Prediction Using Numerical and Binary Features
The model predicts diseases based on the following input features:
- **Numerical Features** (with normal ranges):
  - PLT (Platelets): 0.5 - 450.0
  - RBC (Red Blood Cells): 3.0 - 6.0
  - HGB (Hemoglobin): 10.0 - 20.0
  - WBC (White Blood Cells): 3.0 - 15.0
  - LYMPH (Lymphocytes): 0.5 - 5.0
  - EOS (Eosinophils): 0.0 - 0.5
  - MONO (Monocytes): 0.1 - 1.0
  - NEUT (Neutrophils): 1.0 - 8.0
  - BASO (Basophils): 0.0 - 0.2
- **Binary Features** (0 or 1):
  - ANEHBC (Abnormal Hemoglobin)
  - THROMBOCYTOPENIA (Low Platelet Count)
  - ANERBC (Abnormal Red Blood Cells)
  - LEUKOCYTOSIS (High White Blood Cell Count)

**Output**: After clicking the **Predict** button, the system outputs:
- Predicted disease
- Recommendations including:
  - Treatments
  - Medical suggestions
  - 7-day diet plan
  - Precautions

### 2. Blood Smear Image Analysis
Users can upload a blood smear image to predict the cell type and map it to a disease:
- **Supported Cell Types**:
  - Basophil
  - Eosinophil
  - Erythroblast
  - Lymphocyte
  - Monocyte
  - Platelet
- **Cell-to-Disease Mapping**:
  - Basophil → Basophil high
  - Eosinophil → Eosinophil high
  - Erythroblast → Polycythemia
  - Lymphocyte → Lymphocytosis
  - Monocyte → Monocytes high
  - Platelet → Thrombocytopenia

**Output**: After clicking the **Predict** button, the system outputs:
- Predicted cell type
- Mapped disease
- Recommendations (treatments, diet plan, precautions, etc.)

### 3. Recommendation System
All recommendations (treatments, medical suggestions, 7-day diet plan, and precautions) are generated using **Gemini 2.0 Flash**. Use Your Gemini API Key 

## Project Structure
```
├── .venv/                        # Virtual environment
├── app.py                        # Main application script for numerical/binary feature prediction
├── app2.py                       # Application script (likely for image-based prediction)
├── blood-data-ml-model.ipynb     # Jupyter notebook for ML model development
├── blood-disease-prediction.ipynb # Jupyter notebook for blood disease prediction
├── capped_outlier_boxplots.png   # Visualization of capped outlier boxplots
├── CSV Files/                    # Directory containing dataset CSV files
├── gitattributes                 # Git attributes file
├── haematology.jpg               # Sample image (possibly for documentation or testing)
├── Models/                       # Directory containing pre-trained models
├── outlier_boxplots.png          # Visualization of outlier boxplots
├── requirements.txt              # Project dependencies
├── README.md                     # This file
```

## Prerequisites
- **Python**: Version 3.11
- **Virtual Environment**: Located in `.venv/`
- **Required Libraries**: Listed in `requirements.txt`
- **Gemini 2.0 Flash API**: Required for generating recommendations

## Installation

1. **Clone the Repository** (if applicable):
   ```bash
   git clone <repository-url>
   cd Blood-Disease-Prediction
   ```

2. **Activate the Virtual Environment**:
   ```bash
   cd .venv/Scripts
   activate
   cd ../..
   ```
   On Unix/Linux/Mac:
   ```bash
   source .venv/bin/activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
   *Note*: If `requirements.txt` is incomplete, manually install missing libraries:
   ```bash
   pip install numpy pandas tensorflow scikit-learn pillow
   ```
   For Gemini 2.0 Flash, install the appropriate API package (update `requirements.txt` accordingly).

4. **Verify Python Version**:
   ```bash
   python --version
   ```
   Ensure it outputs `Python 3.11.x`.

## Usage

1. **Prepare Input Data**:
   - For numerical/binary feature prediction, use CSV files in the `CSV Files/` directory or input values via the UI.
   - For image-based prediction, prepare blood smear images (e.g., PNG, JPEG).

2. **Run the Application**:

   - For numerical based and image-based prediction:
     ```bash
     python app2.py
     ```

3. **Interact with the UI**:
   - Enter numerical and binary feature values or upload a blood smear image.
   - Click the **Predict** button to view:
     - Predicted disease (numerical/binary input)
     - Predicted cell type and mapped disease (image input)
     - Recommendations (treatments, 7-day diet plan, precautions, etc.)

## Notes
- The `Models/` directory contains pre-trained models used for predictions.
- Jupyter notebooks (`blood-data-ml-model.ipynb` and `blood-disease-prediction.ipynb`) provide insights into model development and data preprocessing.
- Visualizations (`capped_outlier_boxplots.png` and `outlier_boxplots.png`) are useful for understanding data distributions.

## Contact
For questions or support, reach out via LinkedIn:  
[Shantanu Shinde](https://www.linkedin.com/in/shantanu-shinde-a11b63170/)

## License
This project is licensed under the MIT License.
