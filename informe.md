# 🧠 Laboratorio 3 – Tracking de Modelos de Lenguaje (LLMs) con MLflow

## 🎯 Objetivo
Aplicar **MLflow** para rastrear, comparar y registrar ejecuciones de modelos de lenguaje, analizando sus métricas y comportamiento en diferentes proveedores (Gemini y Ollama).

---

## ⚙️ Parte 3 – Registro y Tracking de LLMs

Se realizaron dos ejecuciones:

1. **Gemini (Google API)**
2. **Ollama (modelo local Llama3.1)**

Durante cada ejecución se registraron:

- **Parámetros:** modelo, temperatura, proveedor y tipo de tarea.  
- **Métricas:** latencia, total de tokens y costo estimado.  
- **Artefactos:** prompts y respuestas generadas.

Ambos modelos se registraron en el **Model Registry** como:

- `llm_gemini_chat`
- `llm_ollama_chat`

Luego se promovieron a los estados **Staging** y **Production**.

---

## 📊 Parte 4 – Análisis comparativo

En la interfaz de MLflow, se compararon las métricas de ambos modelos.

| Modelo | Proveedor | Temperatura | Latencia (s) | Total Tokens | Costo Estimado | Tipo de tarea |
|:--------|:-----------|:-------------|:--------------|:---------------|:----------------|:----------------|
| **Gemini** | Google | 0.7 | 10.61 | 1289 | 0.0019335 | Chat |
| **Ollama** | Local (Llama3.1) | 0.6 | 2.04 | 10 | 0.000001 | Chat |

---

## 🧩 Interpretación de resultados

- 🕓 **Latencia promedio:**  
  El modelo **Ollama (Llama3.1)** tuvo **menor latencia (≈2.0 s)** frente a **Gemini (≈10.6 s)**, debido a que corre localmente sin depender de llamadas HTTP externas.

- 💬 **Cantidad de tokens:**  
  **Gemini** generó **más tokens (1289)**, reflejando una respuesta más extensa y detallada.

- 💸 **Costo estimado:**  
  El costo simulado de Gemini fue mayor, ya que su generación fue más larga y depende de un servicio remoto.

---

## ⚙️ Parámetros a optimizar en futuros experimentos

- **Temperatura:** ajustar entre 0.4–0.8 para equilibrar creatividad y coherencia.
- **Modelo:** probar versiones más ligeras o rápidas (por ejemplo `gemini-1.5-flash` o `llama3.2`).
- **Tamaño del prompt:** reducir longitud para menor latencia y costo.
- **Batching / caching local:** para mejorar tiempos en múltiples inferencias.

---

## ✅ Conclusión

El uso de **MLflow** permitió registrar y comparar fácilmente distintos tipos de modelos (tradicionales y LLMs), visualizar sus métricas en la interfaz y gestionar versiones en el **Model Registry**, demostrando la utilidad del tracking para experimentación reproducible y análisis comparativo entre proveedores.
