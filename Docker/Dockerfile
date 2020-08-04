FROM python:3.9.0b5-alpine3.12

RUN pip install --upgrade pip && pip install flask

WORKDIR /home/microblog
COPY app app
COPY app/microblog.py Docker/entrypoint.sh ./
RUN chmod +x entrypoint.sh

ENV FLASK_APP microblog.py

EXPOSE 5000
ENTRYPOINT ["./entrypoint.sh"]