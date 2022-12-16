FROM python:alpine

COPY ./app/ /app

WORKDIR /app

RUN pip install -r requirements.txt

ENV DEVICE ="dev1"

EXPOSE 5000

ENTRYPOINT [ "python" ]

HEALTHCHECK --interval=5s --timeout=3s CMD curl -f http://localhost:5000

CMD [ "app.py" ]