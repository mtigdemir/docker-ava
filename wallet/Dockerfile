FROM node:lts-alpine

# Install Git 
RUN apk --no-cache add git

# install simple http server for serving static content
RUN npm install -g http-server

RUN git clone https://github.com/ava-labs/ava-wallet.git app

# make the 'app' folder the current working directory
WORKDIR /app

# install project dependencies
RUN npm install

# copy project files and folders to the current working directory
COPY . .

# build app for production with minification
RUN npm run build

EXPOSE 8080

CMD [ "http-server", "dist" ]