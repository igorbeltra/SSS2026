FROM python:3.14-slim
RUN apt-get update && apt-get install -y --no-install-recommends git && rm -rf /var/lib/apt/lists/*
WORKDIR /repo
RUN git clone https://github.com/igorbeltra/SSS2026.git .
WORKDIR /repo/SomeBankingApp/backend
RUN pip install --no-cache-dir -r requirements.txt fastapi
EXPOSE 8000
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]