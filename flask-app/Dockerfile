FROM python:3.11-alpine

WORKDIR /flask-app

# Copy requirements
COPY requirements.txt .

# Install dependencies including gunicorn
RUN pip install --no-cache-dir -r requirements.txt

# Copy app source
COPY . .

# Default command to run the app
CMD ["gunicorn", "-w", "4", "-b", "0.0.0.0:5000", "app:app"]s