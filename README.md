#  Informe README – Aprendiendo Docker

## 📺 Videos revisados
1. [Docker desde cero (video 1)](https://www.youtube.com/watch?v=4Dko5W96WHg)  
2. [Aprende Docker paso a paso (video 2)](https://www.youtube.com/watch?v=CV_Uf3Dq-EU)

---

## 🧠 1. Resumen de los conceptos aprendidos

### 📘 Video 1
Este video explica desde lo más básico qué es Docker y por qué se usa.  
Aprendí que **Docker sirve para crear contenedores**, los cuales son como “cajas” donde se ejecutan las aplicaciones con todas sus dependencias.  
También muestra cómo **instalar Docker**, trabajar con **imágenes** y **contenedores**, usar **Docker Compose** para levantar varios servicios a la vez, y manejar **volúmenes** para guardar datos.  
Al final, enseña cómo usar entornos con *hot reload*, lo que ayuda a ver los cambios del código sin reiniciar todo el contenedor.

### 📗 Video 2
En este video se profundiza en los conceptos. Explica la diferencia entre **Docker y las máquinas virtuales**, mostrando que los contenedores son más ligeros.  
Se aprende a crear imágenes con un **Dockerfile**, usar **docker build** y **docker run**, abrir **puertos**, y compartir imágenes con **docker push**.  
También se enseña cómo usar **docker-compose** para correr varios contenedores al mismo tiempo (por ejemplo, una app y una base de datos).

---

## 💬 2. Reflexión personal

Aprender Docker me pareció muy útil porque **permite ejecutar proyectos sin tener que instalar todo manualmente**.  
Con solo un archivo (`Dockerfile` o `docker-compose.yml`) puedo levantar el entorno igual que mis compañeros.  
Las ventajas que noté son la **rapidez, portabilidad y facilidad para probar aplicaciones**.  
Lo más difícil al principio fue entender los conceptos de imágenes, volúmenes y puertos, pero con práctica se vuelve más claro.  
En general, **Docker facilita mucho el trabajo en equipo y el despliegue de proyectos.**

---

## 🧩 3. Ejemplo práctico: Mi primer contenedor

### Descripción
Creé un contenedor con una pequeña aplicación en **Python** que muestra un mensaje en consola.

### Archivos
**Dockerfile**
```dockerfile
FROM python:3.10
WORKDIR /app
COPY app.py .
CMD ["python", "app.py"]
