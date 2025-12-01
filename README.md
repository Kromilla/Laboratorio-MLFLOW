# 🧠 Proyecto MLflow - Seguimiento y Gestión de Modelos ML

## 📘 Descripción
Proyecto completo de **MLOps** utilizando **MLflow** para el registro, seguimiento y comparación de modelos de Machine Learning tanto clásicos como de lenguaje (LLMs).

### ✨ Características principales
- ✅ Registro y seguimiento de experimentos con MLflow
- ✅ Gestión de parámetros, métricas y artefactos
- ✅ Model Registry para versionado de modelos
- ✅ Implementación de modelos clásicos (Regresión Logística)
- ✅ Integración con LLMs (Google Gemini y Ollama)
- ✅ Comparación de rendimiento entre modelos

---

## 🚀 Inicio Rápido

### 📋 Requisitos previos
- Python >= 3.10  
- pip >= 23  
- Git

### 📦 Instalación

1. **Clonar el repositorio**
```bash
git clone https://github.com/Kromilla/Laboratorio-MLFLOW.git
cd Laboratorio-MLFLOW
```

2. **Crear entorno virtual (recomendado)**
```bash
python -m venv venv
# En Windows:
.\venv\Scripts\activate
# En Linux/Mac:
source venv/bin/activate
```

3. **Instalar dependencias**
```bash
pip install -r requirements
```

---

## 📖 Uso

### 🔬 Ejecutar experimentos

1. **Iniciar MLflow UI**
```bash
mlflow ui
```
Accede a http://localhost:5000 para ver el dashboard

2. **Notebooks disponibles**
- `introduction_mlflow.ipynb` - Introducción básica a MLflow
- `logistic_regression_pipeline.ipynb` - Pipeline de regresión logística
- `MLFLOW_genai_registry.ipynb` - Registro de modelos LLM

### 📊 Estructura del proyecto
```
Laboratorio-MLFLOW/
├── mlruns/              # Experimentos y modelos registrados
├── imgs/                # Imágenes y recursos
├── *.ipynb              # Notebooks de experimentación
├── requirements         # Dependencias del proyecto
└── README.md
```

---

## 🛠️ Tecnologías utilizadas

### Core
- **MLflow** 2.17.0 - Tracking y Model Registry
- **Scikit-learn** - Modelos de ML clásicos
- **Python** >= 3.10

### LLMs
- **Google Generative AI** - Gemini
- **Ollama** - Modelos locales
- **OpenAI** - API de OpenAI

### Utilidades
- PyYAML 6.0.2
- python-dotenv
