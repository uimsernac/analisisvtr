
# Análisis de Reclamos VTR

Este repositorio contiene el análisis de reclamos sobre la empresa VTR. Se incluyen datos recopilados, notebooks de Jupyter para el análisis, y resultados obtenidos.

## Estructura del Repositorio

- **Datos/**: Contiene los datos a analizar. Este directorio está incluido en el `.gitignore` y no se subirá a GitHub.
- **notebooks/**: Contiene los notebooks de Jupyter utilizados para el análisis.
- **resultados/**: Contiene los resultados generados a partir del análisis. Este directorio también está incluido en el `.gitignore`.

## Instrucciones

### Requisitos Previos

- [Python](https://www.python.org/downloads/) (version 3.6 o superior)
- [Jupyter Notebook](https://jupyter.org/install)
- Bibliotecas de Python necesarias (ver `requirements.txt`)

### Instalación

1. Clona el repositorio:
   ```bash
   git clone https://github.com/uimsernac/analisisvtr.git
   cd analisisvtr

### Analisis iniciales 

1. Se unen bases subtel 2019 - 2020 
2. Se aplican filtros criterio subtel
filter_criteria = ["CONTINUIDAD DE SERVICIO", "CONEXIONES A INTERNET", "VELOCIDAD DE INTERNET"]
filtered_df = combined_df[combined_df['Tipo de Motivo'].isin(filter_criteria)]

se analiza la cantidad unica de rut existentes en base filtrada = 4755

proximos pasos:
1. hacer un análisis de texto sobre columna combined_df['Glosa'] para evaluar si existen reclamos asociados a cortes de servicio mayor a 0 horas 
2. volver a analizar la cantidad de ruts unicos -> posibles consumidores afectados 
3. cruzar con bases de datos sernac para obtener listado único de consumidores afectados por cortes en VTR


