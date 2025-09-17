FROM python:3.10-slim-buster

# Set working directory
WORKDIR /code

# Install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir -r requirements.txt

# Copy application source
COPY app /code/app

# Expose service port (adjust if different from 8000)
EXPOSE 8000

# Start the service (FastAPI app)
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]
