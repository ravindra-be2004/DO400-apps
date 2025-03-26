#FROM registry.access.redhat.com/ubi8/nodejs-12
FROM nodejs:latest
#FROM registry.ocp4.example.com:8443/ubi9/nodejs-18-minimal:1-51
# Install dependencies
COPY package.json package-lock.json /app/
WORKDIR /app
USER root
RUN npm ci --production

# Copy app
COPY . /app

EXPOSE 3000
ENTRYPOINT [ "npm", "start" ]
