FROM node:16-alpine

# 安装必要的构建工具和 Python
RUN apk add --no-cache python3 make g++ && \
    ln -sf /usr/bin/python3 /usr/bin/python

# set working directory
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
# start app
CMD ["npm", "run", "serve"]
