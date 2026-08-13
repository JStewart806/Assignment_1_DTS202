FROM python:3.11-slim 

 
RUN useradd -m -u 1001 appuser
 

WORKDIR /app 

 

 

COPY requirements.txt . 

 


RUN pip install -r requirements.txt 

 

 

COPY . . 

 
USER appuser
 

EXPOSE 5000 

 

 

CMD ["python","app.py"] 