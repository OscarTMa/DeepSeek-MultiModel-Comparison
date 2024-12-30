# **DeepSeek Multi-Model Comparison**

## **Description**
This project enables the comparison of multiple language models, such as DeepSeek-V3 and Llama3.1, for tasks like text generation. It features a REST API built with FastAPI for real-time inference and Dockerized deployment for easy scalability.

## **Table of Contents**
- [Description](#description)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## **Project Structure**
```
DeepSeek-MultiModel-Comparison/
├── notebooks/
│   ├── model_comparison.ipynb   # Notebook principal para pruebas y análisis.
├── api/
│   ├── app.py                   # API REST para probar modelos (usando FastAPI o Flask).
│   ├── requirements.txt         # Librerías necesarias para el API.
├── models/
│   ├── load_models.py           # Código para cargar DeepSeek-V3 y otros modelos.
├── datasets/
│   ├── input_data.json          # Datos de entrada para pruebas.
├── results/
│   ├── performance_metrics.csv  # Resultados de métricas.
├── README.md                    # Descripción completa del proyecto.
└── Dockerfile                   # Contenedorización con Docker.

```

## **Installation**

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/DeepSeek-MultiModel-Comparison.git
   cd DeepSeek-MultiModel-Comparison
   ```

2. **Build the Docker container:**
   ```bash
   docker build -t deepseek-api .
   ```

3. **Run the container:**
   ```bash
   docker run -p 8000:8000 deepseek-api
   ```

## **Usage**

1. Access the API at `http://localhost:8000/infer`.

2. Provide the following query parameters:
   - `model_name`: Name of the model (e.g., "deepseek" or "llama").
   - `text`: Input text for generation.

3. Example request using `curl`:
   ```bash
   curl -X GET "http://localhost:8000/infer?model_name=deepseek&text=The+future+of+AI+is"
   ```

## **License**
This project is licensed under the MIT License. See the `LICENSE` file for details.

