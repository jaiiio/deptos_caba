# deptos_caba
Estudio mercado alquiler/venta CABA/GCBA


🏠 Análisis de Datos del Mercado Inmobiliario - CABA
Este proyecto implementa un pipeline de datos profesional utilizando la arquitectura Medallion para procesar y analizar información de departamentos en la Ciudad Autónoma de Buenos Aires. El objetivo es transformar datos crudos (Scraping) en una capa analítica lista para la toma de decisiones.

🚀 Arquitectura del Proyecto
El proyecto se organiza siguiendo las mejores prácticas de Data Engineering, dividiendo la lógica en capas de procesamiento dentro de Databricks:

Bronze (Raw): Ingesta de datos crudos desde archivos CSV utilizando read_files y volúmenes de Unity Catalog. En esta etapa se realiza un filtrado inicial por URL para garantizar la validez de los registros.

Silver (Cleaned): Aplicación de lógica de negocio, normalización de monedas (USD/ARS), tipado de datos numéricos mediante Regex y limpieza de strings (zonas y descripciones).

Gold (Analytics): (En desarrollo) Agregaciones clave como el precio promedio por m² por barrio.

📂 Estructura del Repositorio
La organización del código refleja un flujo de trabajo modular y escalable:

/DDL: Scripts de infraestructura y definición de esquemas. Incluye la configuración del entorno (setup_env), creación de catálogos y definición de tablas.

/ETL: Notebooks encargados del movimiento y transformación de datos entre las capas Bronze y Silver.

/EDA: Análisis Exploratorio de Datos. Contiene la investigación forense de los datos crudos y las visualizaciones que justifican las reglas de limpieza aplicadas.

🛠️ Tecnologías Utilizadas
Databricks (Entorno de cómputo Spark)

SQL (Transformaciones y DDL)

Unity Catalog (Gobernanza de datos y manejo de Volúmenes)

Git / GitHub (Control de versiones)