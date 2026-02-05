FROM python:3.10-slim

WORKDIR /app

# Сначала копируем ТОЛЬКО requirements.txt
COPY requirements.txt .

# Устанавливаем зависимости
RUN pip install --no-cache-dir -r requirements.txt

# Теперь копируем весь код
COPY . .

# Запускаем
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "8000"]