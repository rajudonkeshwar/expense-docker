
# FROM node:20.18.3-alpine3.21
# RUN addgroup -S expense && adduser -S expense -G expense && \
#     mkdir /opt/backend && \
#     chown -R expense:expense /opt/backend
# ENV DB_HOST="mysql"
# WORKDIR /opt/backend
# COPY package.json ./
# COPY *.js ./
# RUN npm install
# USER expense
# CMD ["node", "index.js"]

FROM node:20.18.3-alpine3.21
ENV DB_HOST="mysql"
WORKDIR /opt/backend
COPY package.json ./
COPY *.js ./
RUN npm install
CMD ["node", "index.js"]