FROM node:22-alpine 
 
WORKDIR /app 
 
COPY package*.json ./ 
RUN npm ci --omit=dev 
 
COPY app.js ./ 
 
EXPOSE 3000 
CMD ["node", "app.js"]

docker build -t api-kubernetes:v1 . 
minikube image load api-kubernetes:v1 
minikube image ls