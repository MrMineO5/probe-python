FROM python:3.10

WORKDIR /usr/local/bin

RUN pip install Flask
RUN pip install PyYAML
RUN pip install vertx-eventbus-client

COPY sourceplusplus-*.tar.gz ./sourceplusplus.tar.gz

RUN pip install sourceplusplus.tar.gz

COPY E2ETest.py .

ADD ./spp-probe.yml .

RUN mkdir config
ADD ./config/spp-platform.crt ./config/

CMD ["python", "E2ETest.py"]
