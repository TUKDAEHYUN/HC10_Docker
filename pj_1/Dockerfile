FROM node:20-alpine

RUN apk add --no-cache git

WORKDIR /app

RUN git clone https://github.com/SuperRookiee/WaterMelon-Game.git .

# Yarn 활성화
RUN corepack enable

# 프로젝트 의존성 설치
RUN yarn install --frozen-lockfile

EXPOSE 3000

CMD ["yarn", "dev", "--host", "0.0.0.0"]
