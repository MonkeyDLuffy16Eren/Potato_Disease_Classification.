# 🥔 Potato Disease Classification using Deep Learning

A full-stack ML project for classifying potato leaf diseases using a custom-trained deep learning model. Built with **FastAPI** for the backend and **ReactJS** for the frontend, powered by **TensorFlow** and **Docker-based model serving**.

> ⚠️ Note: This project runs locally. Deployment is not yet set up.

---

## 🛠 Tech Stack

- **Frontend**: ReactJS  
- **Backend**: FastAPI  
- **Model Serving**: TensorFlow Serving (Docker)  
- **Model Training**: Jupyter Notebook + TensorFlow  

---

## 📁 Project Structure




---

## ⚙️ Setup Instructions

### 🔹 Python Environment

1. Install Python (≥3.8)  
2. Install Python dependencies:
   ```bash
   pip3 install -r training/requirements.txt
   pip3 install -r api/requirements.txt
   Install TensorFlow Serving
TensorFlow Serving Setup Guide

 ReactJS Frontend
1. Install Node.js and NPM

2. Install frontend dependencies:

cd frontend
npm install --from-lock-json
npm audit fix
3. Setup environment variables:
  cp .env.example .env

4.Run the frontend:
npm start
🧠 Model Training
Download the dataset from Kaggle (Potato Leaf Disease Dataset)

Keep only folders related to Potatoes

3. Launch Jupyter Notebook:
   jupyter notebook
4. Open:
   training/potato-disease-training.ipynb
5. In Cell #2, update the dataset path

6. Run all cells to train the model

7. Save the trained model into the models/ folder with a version number
🧪 Running the Backend (FastAPI)
✅ Option A: Run API (without TensorFlow Serving)
cd api
uvicorn main:app --reload --host 0.0.0.0
✅ Option B: Run API with TensorFlow Serving
cp models.config.example models.config
2. Run TensorFlow Serving
   docker run -t --rm -p 8501:8501 \
-v C:/Code/potato-disease-classification:/potato-disease-classification \
tensorflow/serving \
--rest_api_port=8501 \
--model_config_file=/potato-disease-classification/models.config
3. Run the FastAPI backend:
   uvicorn main-tf-serving:app --reload --host 0.0.0.0
🔍 Testing the App
Frontend: http://localhost:3000

FastAPI Docs: http://localhost:8000/docs

Model API (if using TF Serving): http://localhost:8501/v1/models/{MODEL_NAME}

👨‍💻 Author
Shreyash Upadhyay
💡 Exploring ML for real-world impact
🌌 Passionate about space + AI
⭐️ Support
If this project helped you, consider giving it a ⭐ on GitHub!


