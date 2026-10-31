<div align="center">

```
 █████╗ ███╗   ██╗██████╗ ██████╗ ███████╗███████╗
██╔══██╗████╗  ██║██╔══██╗██╔══██╗██╔════╝██╔════╝
███████║██╔██╗ ██║██║  ██║██████╔╝█████╗  ███████╗
██╔══██║██║╚██╗██║██║  ██║██╔══██╗██╔══╝  ╚════██║
██║  ██║██║ ╚████║██████╔╝██║  ██║███████╗███████║
╚═╝  ╚═╝╚═╝  ╚═══╝╚═════╝ ╚═╝  ╚═╝╚══════╝╚══════╝
```

**`hardware → algoritmos → software → cloud → ML`**

*Construyo en todas las capas. Del transistor al despliegue, del sensor a la pantalla.*

[![Visitas](https://komarev.com/ghpvc/?username=andres-lopez-g&label=visitas&color=blueviolet&style=flat-square)](https://github.com/andres-lopez-g)
[![Seguidores](https://img.shields.io/github/followers/andres-lopez-g?label=seguidores&style=flat-square&color=blueviolet)](https://github.com/andres-lopez-g?tab=followers)
[![Sitio](https://img.shields.io/badge/sitio-andres--lopez--g.github.io-0a66c2?style=flat-square&logo=githubpages&logoColor=white)](https://andres-lopez-g.github.io)

</div>

---

## $ whoami

Estudiante de ingeniería y desarrollador. Me interesa entender cómo funcionan las cosas
desde adentro: programo microcontroladores, implemento algoritmos desde cero, construyo
herramientas que uso yo mismo y despliego infraestructura real en AWS.

Últimamente el foco está en **cloud**: serverless, contenedores y todo definido como
código con Terraform. Cada proyecto es una excusa para aprender una capa nueva.

- 🔩 **Hardware & IoT** — ESP32, sensores, MicroPython, datos en tiempo real
- 🧮 **Algoritmos** — estructuras de datos, compresión, bajo nivel en C++
- ☁️ **Cloud & Infra** — AWS, Terraform, Lambda, ECS Fargate, DynamoDB
- 🛠️ **Software** — APIs y herramientas en JavaScript / Node.js / Python
- 🤖 **ML** — visión por computadora, modelos en Python

---

## 🚀 Proyectos recientes

### [CVFit](https://github.com/andres-lopez-g/cvfit) · adaptar el CV a una oferta

Pegás tu CV (texto o PDF) y una oferta de trabajo; la app devuelve el CV reescrito con el
vocabulario de la oferta, un score de match 0–100 con las palabras clave faltantes y un
tip de entrevista. **No inventa experiencia**: solo reordena hechos que ya están en el CV.

- 100 % serverless: S3 estático → API Gateway → Lambda (Node 22) → **Bedrock / Nova Pro**
- El PDF viaja en base64 y se pasa a Bedrock como bloque `document` (sirve para escaneados)
- Costo real por consulta medido con **CloudWatch Embedded Metric Format**, sin base de datos
- Terraform modular con estado remoto en S3 + locks en DynamoDB

`AWS` · `Terraform` · `Bedrock` · `Lambda` · `API Gateway` · `JavaScript`

### [comp-nube](https://github.com/andres-lopez-g/comp-nube) · miniaturas serverless en AWS

Subís una imagen a un sitio estático en S3 y en menos de un minuto aparece la miniatura:
S3 → evento → **Lambda** → `ecs:RunTask` → **ECS Fargate** (Pillow) → S3.

- Sin ECS Service: el contenedor **solo existe mientras procesa** y se apaga al terminar
- La ruta del objeto y el bucket llegan al contenedor por variables de entorno
- Frontend vanilla sin SDK, buckets públicos por ser un parcial (en producción: privados +
  URLs firmadas)
- Todo desplegable y borrable con Terraform, sin pasos manuales

`AWS` · `Terraform` · `ECS Fargate` · `Lambda` · `Docker` · `Python`

### [CarScan](https://github.com/andres-lopez-g/CarScan) · buscador de vehículos en Colombia

Agrega publicaciones de varios marketplaces, normaliza precios, puntúa las mejores ofertas
y las muestra en un mapa con distancia desde tu ubicación.

- Backend **FastAPI** + **PostgreSQL/PostGIS**, scrapers con Playwright y BeautifulSoup
- Frontend **Next.js 14** + TypeScript + Leaflet sobre OpenStreetMap
- Scraping responsable: rate limiting, sin bypass de captchas, siempre enlazando el original
- Todo levantable con `docker compose up`

`Python` · `FastAPI` · `Next.js` · `PostGIS` · `Docker`

---

## 📦 Proyectos anteriores

| Proyecto | Descripción | Stack |
|:---|:---|:---|
| [**AsisT**](https://github.com/andres-lopez-g/AsisT) | Asistente personal: finanzas, archivos y planeación del día | JS / Node.js |
| [**esp32-meteorologia**](https://github.com/andres-lopez-g/esp32-meteorologia) | Estación meteorológica con ESP32, DHT11, MQ-135, BMP180 y ThingSpeak | MicroPython / IoT |
| [**huffman-compression**](https://github.com/andres-lopez-g/huffman-compression) | Compresor de archivos con el algoritmo de Huffman, desde cero | C++ |
| [**ml-face-censor**](https://github.com/andres-lopez-g/ml-face-censor) | Detección y censura automática de rostros en imágenes | Python / ML |
| [**API-gobierno**](https://github.com/andres-lopez-g/API-gobierno) | Datos abiertos de datos.gov.co → MySQL → API Flask → frontend React | Python / React |
| [**final-bdd2**](https://github.com/andres-lopez-g/final-bdd2) | Base de datos poliglota: PostgreSQL + Neo4j en el mismo proyecto | Python / SQL |
| [**torredebabel**](https://github.com/andres-lopez-g/torredebabel) | Juego construido en Python y SQL para taller de lenguajes | Python / SQL |

---

## 🔧 Con qué trabajo

<div align="center">

**Lenguajes**

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)

**Cloud & herramientas**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

**Hardware & ML**

![ESP32](https://img.shields.io/badge/ESP32-FF6600?style=flat-square)
![MicroPython](https://img.shields.io/badge/MicroPython-2B5B84?style=flat-square&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)

</div>

---

<div align="center">
  <img src="https://streak-stats.demolab.com?user=andres-lopez-g&theme=tokyonight&hide_border=true&date_format=j%20M%5B%20Y%5D" alt="Racha de contribuciones en GitHub" />
</div>

---

<div align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=andres-lopez-g&theme=tokyo-night&hide_border=true&area=true" alt="Actividad en GitHub" />
</div>

---

## 📫 Hablemos

Abierto a colaborar en proyectos de **cloud, backend, IoT o ML** —y a cualquier problema
que valga la pena resolver.

<div align="center">

[![GitHub](https://img.shields.io/badge/github/andres--lopez--g-121013?style=for-the-badge&logo=github&logoColor=white)](https://github.com/andres-lopez-g)
[![Sitio](https://img.shields.io/badge/sitio-web-0a66c2?style=for-the-badge&logo=githubpages&logoColor=white)](https://andres-lopez-g.github.io)

</div>
