FROM python:3.10-slim

WORKDIR /app

# Install system dependencies
RUN apt-get update && apt-get install -y --no-install-recommends gcc && rm -rf /var/lib/apt/lists/*

# Copy and install Python dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt gunicorn

# Copy application files
COPY . .

# Expose backend application port
EXPOSE 8080

# Run Flask application with Gunicorn production server
CMD ["gunicorn", "--bind", "0.0.0.0:8080", "app:app"]