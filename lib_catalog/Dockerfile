FROM python:3.9 
WORKDIR /usr/src/app
ENV PYTHONBUFFERED 1
COPY . .
RUN pip install --no-cache-dir -r requirements.txt
EXPOSE 8000
CMD ["./run_app.sh"]



