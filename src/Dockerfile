FROM node:18.11.0
# set working directory
WORKDIR /app
# add package for install node modules
COPY package*.json ./
RUN npm install
# add app
COPY . .
EXPOSE 8080
CMD ["node", "server.js"]