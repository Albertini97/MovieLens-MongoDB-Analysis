🎬 MovieLens-MongoDB-Analysis

Este proyecto analiza el conjunto de datos MovieLens utilizando MongoDB Atlas y Google Colab. Se realizan consultas avanzadas con PyMongo para identificar patrones en calificaciones de películas y preferencias de usuarios.

✨ Características del Proyecto

⛏ Uso de MongoDB Atlas para almacenar y gestionar datos.

⚙ Consultas avanzadas con PyMongo.

📊 Análisis y visualización de datos con Pandas y Matplotlib.

⭐ Identificación de géneros más populares y usuarios activos.

📰 Reporte detallado de los hallazgos y tendencias.

📚 Estructura del Repositorio

📂 MovieLens-MongoDB-Analysis
 ├── 📜 README.md  # Explicación del proyecto
 ├── 📜 requirements.txt  # Librerías necesarias
 ├── 📜 notebook.ipynb  # Análisis en Google Colab
 ├── 📂 scripts  # Código Python para consultas avanzadas
 ├── 📂 data  # Datos (opcional, mejor referenciar si son pesados)

📚 Instalación

Clona el repositorio:

git clone https://github.com/TU_USUARIO/MovieLens-MongoDB-Analysis.git
cd MovieLens-MongoDB-Analysis

Instala las dependencias:

pip install -r requirements.txt

Ejecuta el notebook en Google Colab o Jupyter Notebook.

💡 Uso

Ejecutar consultas sobre el dataset de MovieLens.

Analizar patrones de calificaciones por género y usuarios.

Visualizar resultados con gráficos.

🌟 Ejemplo de Consulta en MongoDB

from pymongo import MongoClient

client = MongoClient("mongodb+srv://usuario:password@cluster.mongodb.net/movielens")
db = client['movielens']

# Películas de género 'Comedy'
comedy_movies = db.movies.find({"genres": {"$regex": "Comedy", "$options": "i"}})
for movie in comedy_movies:
    print(movie["title"])

📖 Dataset

Los datos provienen del conjunto MovieLens de la Universidad de Minnesota:

Películas: Títulos, año de estreno, géneros.

Calificaciones: Registros de usuarios (0.5 - 5.0 estrellas).

Etiquetas: Palabras clave asignadas por usuarios.

📅 Fuente: MovieLens Dataset

👌 Contribuciones

Si deseas mejorar este proyecto, ¡eres bienvenido/a! Puedes:

Hacer un fork del repositorio.

Crear una nueva rama (git checkout -b nueva-rama).

Realizar mejoras y subir cambios (git commit -m "Mejora X").

Crear un pull request.

🏆 Licencia

Este proyecto está bajo la licencia MIT. Puedes usarlo y modificarlo libremente.

🎥 Desarrollado por: Alberto💻 Contacto: https://www.linkedin.com/in/alberto-labarta-holgado

