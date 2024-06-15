# Data Quality - Perfilamiento de datos (Data Profiling)

## Hi there 👋, I'm Cesar (@Cesarandres91)

- 👀 I’m interested in data quality, data science, and data governance.
- 🌱 I’m currently improving my skills in data science.
- 💞️ I’m looking to collaborate on data governance, quality, science or cybersecurity projects.
- 📫 How to reach me: [LinkedIn](https://www.linkedin.com/in/andreschile/)


Te será muy útil si se eres : 
| Position                                                         |
|---------------------------------------------------------------|
| 🧑‍🔬 Científico de Datos (Data Scientist)                  |
| 👷‍♂️ Ingeniero de Datos (Data Engineer)                    |
| 📊 Analista de Datos (Data Analyst)                          |
| 🗄️ Administrador de Bases de Datos (Database Administrator)  |
| 🏗️ Arquitecto de Datos (Data Architect)                    |
| 🛠️ Ingeniero de Calidad de Datos (Data Quality Engineer)   |
| 💡 Ingeniero de BI (Business Intelligence Engineer)          |
| 📈 Analista de BI (Business Intelligence Analyst)            |
| 💼 Consultor de Datos (Data Consultant)                     |

# Sistema de Perfilamiento de Datos para BigQuery

## Descripción del Proyecto
Este repositorio contiene un marco de trabajo automatizado diseñado para crear perfilamiento de datos de tablas almacenadas en Google BigQuery de manera masiva, completa, rápida y eficiente (puede ser aplicable también a Athena de AWS con algunas modificaciones).

## :mag_right: Análisis Detallado y Calidad de datos
El proyecto incorpora funcionalidades avanzadas para generar consultas SQL detalladas y específicas que se ejecutan en BigQuery. Estas consultas no solo contabilizan registros totales y nulos, sino que también evalúan la integridad y la distribución de los datos, incluyendo la identificación de valores extremos y la realización de cálculos estadísticos como promedios y conteos condicionales. Esto es esencial para garantizar que los datos no solo sean precisos, sino también útiles para tomar decisiones informadas e identifica posibles outliers.

## :hammer_and_wrench: Flexibilidad y Manejo Eficiente
Los datos pueden cargarse de fuentes diferentes mientas cumplan el formato del template como archivos CSV, Excel o googlesheet, además su capacidad para automatizar el desglose de grandes conjuntos de datos en múltiples partes facilita su manejo y análisis para mejorar el rendimiento, manejo de recursos y control de limites que establece BigQuery.

## :handshake: Invitación a Colaborar
Invito a todos los interesados en mejorar la calidad de sus datos y eficientizar sus procesos analíticos a conectarse conmigo para explorar posibles colaboraciones y oportunidades profesionales. Juntos, podemos transformar la manera en que interactuamos con los datos y liderar la próxima ola de innovaciones en la analítica de datos.

## :sparkles: Gracias por su atención y espero poder conectar y colaborar con muchos de ustedes en el futuro próximo. :sparkles:

## 📁 Estructura de Archivos

Asegúrate de tener estos archivos en tu directorio de trabajo:
- `perfilamiento_proyecto_dq_desktop.py`:  Este archivo contiene todo el código necesario para ejecutar las consultas de perfilamiento en el escritorio con Python.
- `perfilamiento_proyecto_dq_gcolab.py`:  Este archivo contiene todo el código necesario para ejecutar las consultas de perfilamiento en google colab.
- `plantilla_perfilamiento.csv`: Una plantilla CSV que define el esquema de los datos a analizar.
  
- ## Uso
- Modifica el archivo `perfilamiento_datos.csv` con los campos y parámetros deseados para el perfilamiento.
- Ejecuta el script `perfilamiento_proyecto_dq.py` para generar las consultas SQL

## 🗺️ Guía Paso a Paso

### Paso 1: Preparar la Plantilla de Datos

1. Abre el archivo `perfilamiento_datos.csv` en un editor de texto o en una hoja de cálculo.
2. Edita las columnas según los datos que necesitas perfilar:
   - **CAMPO**: Nombre del campo a analizar.
   - **TIPO**: Tipo de dato del campo (e.g., STRING, INTEGER).
   - **PARTICION**: Nombre de la columna de partición.
   - **TABLA**: Nombre de la tabla donde se encuentra el campo.
   - **Fecha_desde**: Fecha de inicio para el filtro de la consulta.
   - **Fecha_hasta**: Fecha de fin para el filtro de la consulta.

     Ejemplo del archivo:
     ![image](https://github.com/Cesarandres91/DQ_Perfilamiento_de_datos_en_Bigquery/assets/102868086/8fcbe9e9-3378-48cb-bdcc-04038de2ae87)


### Paso 2: Configuración del Entorno

Asegúrate de que tu entorno Python está configurado correctamente, siempre puedes ejecutarlo en googlecolab para evitar quebraderos de cabeza y verifica que tienes las credenciales necesarias para acceder a Google BigQuery.

### Paso 3: Ejecutar el Script

1. Abre tu terminal o línea de comandos.
2. Navega hasta el directorio donde se encuentran los archivos `perfilamiento_proyecto_dq.py` y `perfilamiento_datos.csv`.
3. Ejecuta el siguiente comando:
   ```bash
    perfilamiento_proyecto_dq_desktop.py
   ```
   o desde google colab puedes usar el otro código
   
   ```bash
   perfilamiento_proyecto_dq_gcolab.py
   ```
   
El script leerá la plantilla (recuerda ajustar el directorio), generará las consultas SQL en un archivo de texto que podrás copiar y pegar en BigQuery.

Ejemplo Query generada: 
``` Ejemplo_Query_generada.txt ```
![image](https://github.com/Cesarandres91/DQ_Perfilamiento_de_datos_en_Bigquery/assets/102868086/846bcea7-572f-4f27-be47-d41e990c5c3f)

PD: Las consultas están particionadas en varios archivos en caso de que la cantidad de campos sea alta, para mejorar el rendimiento, manejo de recursos y control de limites que establece BigQuery, pero puedes modificarlo directamente en el código en caso de que no lo necesites.

### Paso 4: Revisar los Resultados
Revisa los resultados de las consultas que se mostrarán en la salida estándar o en los archivos de salida especificados en el script.
Analiza los datos para entender mejor la calidad y estructura de los datos en tu base de datos BigQuery.

![image](https://github.com/Cesarandres91/DQ_Perfilamiento_de_datos_en_Bigquery/assets/102868086/a87a847e-3a5a-44b0-ab85-20997af8381a)

![image](https://github.com/Cesarandres91/DQ_Perfilamiento_de_datos_en_Bigquery/assets/102868086/0121ddfc-0de8-41c9-a449-9ea17c2589eb)

### Visualización:
Ya con estos datos, solo queda generar las gráficas con nuestra herramientas de inteligencia de negocio preferida o plataforma de visualización de datos,
generalmente en las compañías utilizamos Tableau o Power BI para generar tableros de control utilizando como input la tabla final,
pero para este caso y no depender de ninguna licencia generé las gráficas solu utilizando python, con estas librerías:
```
import matplotlib.pyplot as plt
import seaborn as sns
# Configurar estilo de Seaborn
sns.set(style="whitegrid")
 ```
![Nulos](https://github.com/Cesarandres91/DQ_Perfilamiento_de_datos_en_Bigquery/assets/102868086/60a98605-165d-4d1a-87d0-7d6584313fb9)

![Distintos](https://github.com/Cesarandres91/DQ_Perfilamiento_de_datos_en_Bigquery/assets/102868086/4fad40d0-29c3-4a22-8047-16ecae79c166)

![Largo_maximo](https://github.com/Cesarandres91/DQ_Perfilamiento_de_datos_en_Bigquery/assets/102868086/2888a304-eccc-41dc-ab4e-78890a18537d)

![Largo_minimo](https://github.com/Cesarandres91/DQ_Perfilamiento_de_datos_en_Bigquery/assets/102868086/a735da08-c44f-41e0-8617-9fc2e050acc8)


🧐 Solución de Problemas
Si encuentras errores durante la ejecución, verifica lo siguiente:
Que las credenciales de BigQuery están configuradas correctamente.
Que los nombres de las columnas en perfilamiento_datos.csv coinciden exactamente con los de la base de datos.
Que tienes permisos suficientes en BigQuery para ejecutar consultas y acceder a las tablas especificadas.

## Características
- **Generación Automática de Consultas SQL**: Scripts de Python leen especificaciones desde una hoja de Excel y generan consultas SQL.
- **Perfilamiento Personalizable**: Permite la personalización completa del perfilamiento basado en parámetros definidos en la hoja de Excel.
- **Reportes de Calidad de Datos**: Genera métricas de calidad de datos como registros correctos, errores y umbrales de calidad.

## Pre-requisitos
- Python 3.8 o superior.
- Acceso a Google BigQuery.
- Google Colab o un entorno Python local configurado.
- Paquete `pandas` instalado para la manipulación de datos.
- Credenciales de Google Cloud con permisos adecuados para leer y ejecutar consultas en BigQuery.

## Configuración
1. **Clonar el Repositorio**:

2. **Instalación de Dependencias**:


3. **Configuración de Credenciales de Google Cloud**:
- Asegúrate de tener un archivo de credenciales de servicio de Google Cloud (JSON).
- Establece la variable de entorno `GOOGLE_APPLICATION_CREDENTIALS` apuntando al archivo JSON:
  ```
  export GOOGLE_APPLICATION_CREDENTIALS="path/to/your/credentials.json"
  ```


## Contribución
Para contribuir al proyecto, por favor sigue los siguientes pasos:
- **Fork el Repositorio**: Haz un fork del proyecto a tu cuenta de GitHub.
- **Crea una Rama**: Crea una rama para tus cambios.
- **Haz tus Cambios**: Añade o mejora funcionalidades.
- **Envía un Pull Request**: Envía un PR para integrar tus cambios al repositorio principal.

## Licencia
Este proyecto está licenciado bajo la Licencia MIT - ver el archivo `LICENSE` para más detalles.


