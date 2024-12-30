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
├── app.py                   # API with FastAPI
├── Dockerfile               # Dockerfile for containerization
├── requirements.txt         # Project dependencies
└── README.md                # Project documentation
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

