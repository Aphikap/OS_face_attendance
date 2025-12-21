FROM python:3.10-slim
WORKDIR /app

RUN apt-get update && apt-get install -y --no-install-recommends \
  tzdata \
  build-essential gcc g++ gfortran \
  pkg-config \
  libopenblas-dev \
  && rm -rf /var/lib/apt/lists/*

ENV TZ=Asia/Bangkok

COPY requirements.txt .


RUN python -m pip install --upgrade pip setuptools wheel

RUN pip install --no-cache-dir --prefer-binary -r requirements.txt

COPY . .

EXPOSE 5000
CMD ["python", "api.py"]
