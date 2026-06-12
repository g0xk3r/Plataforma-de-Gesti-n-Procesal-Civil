# Usamos una versión ligera de Node.js
FROM node:18-alpine

# Creamos el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiamos solo los archivos de dependencias primero (optimiza el caché de Docker)
COPY package*.json ./

# Instalamos las dependencias
RUN npm install

# Copiamos el resto del código del servidor
COPY . .

# Exponemos el puerto que usa tu API
EXPOSE 3001

# Comando para iniciar tu servidor
CMD ["node", "index.js"]