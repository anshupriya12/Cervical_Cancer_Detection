# Cervical Cancer Detection

This project was originally built as a deep learning notebook for Pap smear classification. It is now prepared for Streamlit deployment.

## What was added
- `app.py`: Streamlit web app for image upload and prediction
- `requirements.txt`: Python dependencies for deployment

## How to deploy on Streamlit Cloud
1. Push this repository to GitHub.
2. Open https://streamlit.io/
3. Choose "Deploy an app"
4. Connect your GitHub account and select this repository.
5. Set the main file to `app.py`.
6. Click Deploy.

## Important note about the model
The notebook contains the model architecture and training logic, but the repository does not currently include a saved `.keras` or `.h5` model file. The app will still run with a placeholder ResNet101V2 model, but for real predictions you need to save your trained model as one of these files:

- `model/cervical_cancer_model.keras`
- `model/cervical_cancer_model.h5`

After saving the trained model, Streamlit will automatically use it when the app starts.

## Run locally
```bash
pip install -r requirements.txt
streamlit run app.py
```
