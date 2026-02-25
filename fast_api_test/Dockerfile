FROM python:3.9-slim

RUN addgroup -S appgroup && user -S appuser -G appgroup

WORKDIR /app

RUN chown -R appuser:appgroup /app 

USER appuser

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY test.db /app/test.db

COPY . .

EXPOSE 8000

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]