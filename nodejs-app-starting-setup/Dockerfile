# 운영체제 레이어.
FROM node 

# 가상의 작업공간 레이어
WORKDIR /app

# 복사를 할 경로 및 폴더
COPY . /app

# 실행이 되는 명령
RUN npm install

# 열어줄 포트
EXPOSE 80

# 이미지가 빌드될 때 실행되지 않고 추후에 컨테이너가 실행될 때 작동할 명령
CMD [ "node", "server.js" ]