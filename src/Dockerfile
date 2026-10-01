FROM node:26.9.0-alpine3.24
RUN adduser -D appuser
WORKDIR /app
RUN chown -R appuser /app
USER appuser
COPY --chown=appuser:appuser package*.json ./
RUN npm install
COPY --chown=appuser:appuser . .
EXPOSE 8080
CMD ["node", "server.js"]

