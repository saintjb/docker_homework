FROM python:3.9-bullseye
WORKDIR /app
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1
COPY . .
RUN chmod +x run.sh && pip install -r requirements.txt
EXPOSE 8000
ENTRYPOINT ["/bin/bash", "-c", "./run.sh" ]



