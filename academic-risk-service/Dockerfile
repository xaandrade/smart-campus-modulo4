# Usamos una imagen liviana de Python oficial
FROM python:3.10-slim

# Definimos la carpeta de trabajo dentro del contenedor
WORKDIR /app

# Copiamos la lista de librerías e instalamos
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copiamos todo el código del microservicio dentro del contenedor
COPY . .

# Exponemos el puerto en el que escuchará FastAPI
EXPOSE 8001

# Comando para arrancar el servidor cuando el contenedor se encienda
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8001"]