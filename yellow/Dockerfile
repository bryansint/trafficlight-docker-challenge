###################################################################
# This is templating file of Dockerfile. It will help you to      #
# complete all required instructions for building the Dockerfile. #
###################################################################

# 1.1.1 Utilice la imagen base node:17.0-alpine3.14
FROM node:17.0-alpine3.14

# 1.1.2 Establecer el directorio de trabajo en el contenedor como /app
WORKDIR /app

# 1.1.3 Copiar los archivos package*.json al directorio de trabajo /app
COPY package*.json ./

# 1.1.4 Instalar el administrador de paquetes npm usando apk
RUN apk add --no-cache npm=7.17.0-r0 && \
    npm install

# 1.1.5 Copiar el archivo app.js al directorio de trabajo
COPY app.js ./

# 1.1.6 Copiar los archivos index.pug y favicon.ico al directorio /app/views/
COPY views/index.pug views/
COPY views/favicon.ico views/

# 1.1.7 Exponer el puerto 80 en todos los contenedores
EXPOSE 80

# 1.1.8 Ejecutar el siguiente comando en tiempo de ejecución: node app.js
CMD ["node", "app.js"]
