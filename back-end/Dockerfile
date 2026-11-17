FROM node:20-alpine

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm install --only=production

COPY . .

# Passa all'utente non-root per sicurezza (Docker Hardening)
USER node

EXPOSE 3000
CMD ["node", "server.js"]