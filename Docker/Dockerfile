FROM python:3.9.0b5-alpine3.12

WORKDIR /home/microblog
COPY app app
COPY requirements.txt .flaskenv config.py microblogapp.py Docker/entrypoint.sh ./
RUN chmod +x entrypoint.sh

RUN pip install --upgrade pip && pip install -r requirements.txt

EXPOSE 5000
ENTRYPOINT ["./entrypoint.sh"]