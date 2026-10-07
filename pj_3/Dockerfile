FROM node:14-alpine

RUN apk add --no-cache git

WORKDIR /app

RUN git clone https://github.com/rjanjic/js-minesweeper.git .

# package.json의 dev 서버를 3000 포트로 고정
RUN sed -i 's#"dev": "webpack-dev-server --content-base public"#"dev": "webpack-dev-server --content-base public --host 0.0.0.0 --port 3000"#' package.json

# Yarn 활성화
RUN corepack enable

# 프로젝트 의존성 설치
RUN yarn install --frozen-lockfile

EXPOSE 3000

CMD ["yarn", "dev"]
