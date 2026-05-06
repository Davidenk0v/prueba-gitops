# Imagen base ligera
FROM node:18-alpine

# Directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar dependencias primero (aprovecha la caché de Docker)
COPY package.json .
RUN npm install --omit=dev

# Copiar el resto del código
COPY index.js .

# Puerto que expone el contenedor
EXPOSE 3000

# Variables de entorno por defecto
ENV PORT=3000
ENV APP_VERSION=v1

# Comando de arranque
CMD ["node", "index.js"]
