#  Informe README – Docker
<img width="659" height="440" alt="image" src="https://github.com/user-attachments/assets/e519960b-d9b0-4e89-aac5-53f547a0915e" />


## Estos son los vídeos que nos brindó el instructor, en base a ellos se hace este informe.
1. [Aprende Docker ahora(video 1)](https://www.youtube.com/watch?v=4Dko5W96WHg)  
2. [Docker de novato a pro (video 2)](https://www.youtube.com/watch?v=CV_Uf3Dq-EU)

---

##  1. Resumen de los conceptos aprendidos

Estos explican desde lo más básico, como qué es Docker y por qué se usa.  
Aprendí que **Docker sirve para crear contenedores**, los cuales son como “cajas” donde se ejecutan las aplicaciones con todas sus dependencias.  
También muestran cómo **instalar Docker**, trabajar con **imágenes** y **contenedores**, usar **Docker Compose** para levantar varios servicios a la vez, y manejar **volúmenes** para guardar datos.  
Al final, en uno de los vídeos enseña a cómo usar entornos con *hot reload*, lo que ayuda a ver los cambios del código sin reiniciar todo el contenedor lo cuál es muy útil.
También profundizan en los conceptos. Explican la diferencian entre **Docker y las máquinas virtuales**, mostrando que los contenedores son más ligeros.  
Se aprende a crear imágenes con un **Dockerfile**, usar **docker build** y **docker run**, abrir **puertos**, y compartir imágenes con **docker push**.  
También se enseña cómo usar **docker-compose** para correr varios contenedores al mismo tiempo (por ejemplo, una app y una base de datos).

---

## 💬 2. Reflexión personal

Aprender Docker me pareció muy útil porque **permite ejecutar proyectos sin tener que instalar todo manualmente**, con solo un archivo (`Dockerfile` o `docker-compose.yml`) puedo levantar el entorno igual que mis compañeros diría que las ventajas son la **rapidez y facilidad para probar aplicaciones**.  
Lo más difícil al principio y lo que aún me parece un poco confuso fue entender los conceptos de imágenes, volúmenes y puertos, pero con práctica se puede llegar a volver más claro.  
Y en general, **Docker facilita mucho el trabajo en equipo que es a lo que están sometidos todos los desarrolladores y el despliegue de proyectos.**

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
