FROM python:3.10-slim
WORKDIR /app

# [NEW] ติดตั้ง tzdata และตั้งค่า Timezone เป็น Asia/Bangkok
RUN apt-get update && apt-get install -y tzdata
ENV TZ=Asia/Bangkok

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
EXPOSE 5000
CMD ["python", "api.py"]