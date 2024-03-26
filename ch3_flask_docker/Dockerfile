FROM python:3.8

# 인수 지정
ARG VERSION
LABEL org.label-schema.version=${VERSION}
# 모델이 학습되어 컨테이너 이미지에 포함된 시점부터 오래 지남
# 이런 경우, 컨테이너에 직접 접속해서 모델 파일을 확인하는 것 보다 레이블 확인하면 편함

RUN python3 -m pip install --upgrade pip

# requirements.txt를 컨테이너의 지정경로에 복사
COPY ./requirements.txt /ws/requirements.txt

WORKDIR /ws

RUN pip install -r requirements.txt

COPY ./webapp/ /ws

ENTRYPOINT [ "python3" ]

CMD [ "app.py" ]