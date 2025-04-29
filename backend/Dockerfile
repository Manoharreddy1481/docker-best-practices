FROM node:20-alpine
EXPOSE 8080
ENV DB_HOST="mysql"
RUN addgroup -S expense && expense -G expense
#ENV DB_HOST="localhost" #Host Network
#ENV DB_HOST="mysql" Bridge Network
RUN mkdir /opt/server
RUN chown -R /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
USER expense
CMD [ "node", "index.js" ]


#Before best practices implemented
# FROM node:20
# EXPOSE 8080
# ENV DB_HOST="mysql"
# #ENV DB_HOST="localhost" #Host Network
# #ENV DB_HOST="mysql" Bridge Network
# RUN mkdir /opt/server
# WORKDIR /opt/server
# COPY package.json .
# COPY *.js .
# RUN npm install
# CMD [ "node", "index.js" ]

