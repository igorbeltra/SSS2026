FROM node:20-alpine
RUN apk add --no-cache git
WORKDIR /repo
RUN git clone https://github.com/igorbeltra/SSS2026.git .
WORKDIR /repo/SomeBankingApp/frontend
RUN npm ci
EXPOSE 4200
CMD ["npx", "ng", "serve", "--host", "0.0.0.0"]