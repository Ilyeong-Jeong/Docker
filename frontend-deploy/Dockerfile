FROM node:14-alpine

# Create app directory
RUN mkdir -p /usr/src/app

# Move app directory
WORKDIR /usr/src/app

# Production mode
ENV NODE_ENV=production

# Copy source
COPY server.js package.json ./

COPY dist ./dist

RUN npm install --production

# listing
RUN file="$(ls -1 /usr/src/app)" && echo $file
RUN echo $(ls -1 /usr/src/app)

# OPEN port
EXPOSE <노출시킬 포트번호>

# Run command
CMD [ "npm", "run", "start" ]