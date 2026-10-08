FROM node:21-alpine3.17

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

ARG REACT_APP_API_BASE_URL
ENV REACT_APP_API_BASE_URL=$REACT_APP_API_BASE_URL

RUN  npm run build

EXPOSE 3000

CMD ["npx", "serve","-s", "build", "-l", "tcp://0.0.0.0:3000"]