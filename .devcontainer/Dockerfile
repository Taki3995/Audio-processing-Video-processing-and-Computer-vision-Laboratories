# 1. Imagen base oficial y ligera de Python
FROM python:3.11-slim

# 2. Variable de entorno para evitar pausas interactivas en la consola
ENV DEBIAN_FRONTEND=noninteractive

# 3. Instalación de dependencias del sistema operativo (C++, utilidades multimedia para audio y video)
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    ffmpeg \
    libsndfile1 \
    git \
    && rm -rf /var/lib/apt/lists/*

# 4. Actualización del gestor pip e instalación de librerías científicas. Agregar si tengo que instalar nuevas cosas
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir \
    numpy \
    scipy \
    matplotlib \
    scikit-image \
    ipykernel