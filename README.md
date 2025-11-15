# 🧠 Laboratorio 3 – LLMs con MLflow

## 📘 Descripción general
Este laboratorio tiene como objetivo aplicar **MLflow** para el registro, seguimiento y comparación de modelos tanto clásicos como de lenguaje (LLMs).  
Se implementó el ciclo completo de *Machine Learning Operations (MLOps)*, incluyendo:

- Registro de experimentos y runs.
- Seguimiento de parámetros y métricas.
- Registro y promoción de modelos en el **Model Registry**.
- Comparación entre modelos clásicos y modelos de lenguaje (Gemini y Ollama).

---

## ⚙️ Dependencias y entorno

### 🧩 Requisitos principales
- Python >= 3.10  
- pip >= 23  
- Virtualenv (opcional)

📄 **[Ver informe completo](informe.md)**

### 📦 Librerías utilizadas
```bash
mlflow==2.17.0
PyYAML==6.0.2
scikit-learn
ollama
openai
google-generativeai
dotenv
os
