FROM python:3.8-slim
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1
COPY resources.txt .
RUN python -m pip install -r resources.txt
WORKDIR /app
COPY . /app
RUN adduser -u 5678 --disabled-password --gecos "" appuser && chown -R appuser /app
USER appuser
CMD ["python", "api.py"]
