FROM node:20

WORKDIR /usr/src/app

# 1) 의존성
COPY package*.json ./
RUN npm ci || npm install
RUN npm run prepare

# 2) 설정 + 소스
COPY tsconfig.json ./
COPY src ./src

# 3) 빌드 & 런
RUN npm run build

EXPOSE 3000
CMD ["npm","run","start:prod"]
