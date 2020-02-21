FROM tiangolo/uwsgi-nginx-flask

WORKDIR /app
COPY ./src /app
RUN pip install -r requirements.txt
EXPOSE 3000

ENTRYPOINT ["uwsgi", "--socket", "0.0.0.0:3000", "--protocol=http", "-w", "wsgi:app"]