FROM node:20.10.0-slim
WORKDIR /app
COPY package*.json ./
RUN npm install
RUN apt update && apt install -y stress && npm install
COPY . .
RUN npm run compile
EXPOSE 3000
CMD ["npm", "start"]


