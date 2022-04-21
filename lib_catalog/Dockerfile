FROM python:3.9
WORKDIR /app
COPY . .
EXPOSE 8000
RUN chmod +x run.sh && pip install -r requirements.txt 
ENTRYPOINT [ "/bin/bash", "-l", "-c", "./run.sh"]


