# ── inference_services/model3/Dockerfile ──
FROM deepanshu0903/nst_app:tf-base

WORKDIR /app

# Install only model-3’s minimal requirements
COPY requirements.txt /app/requirements.txt
RUN pip install --no-cache-dir --upgrade pip \
    && pip install --no-cache-dir -r /app/requirements.txt

COPY ./app /app

EXPOSE 8000
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
