# Resumen del Proyecto: Análisis de Hipotecas en España

## 🔍 Vista Rápida
| **Aspecto**          | **Detalle**                                                                 |
|-----------------------|----------------------------------------------------------------------------|
| **Objetivo**          | Analizar tendencias de hipotecas por número/importe, región y tipo de finca |
| **Fuente de datos**   | [Instituto Canario de Estadística]([https://datos.canarias.es/...](https://datos.canarias.es/catalogos/general/dataset/nuevas-hipotecas-constituidas-segun-naturaleza-de-la-finca-comunidades-autonomas-y-provincias-p) (214k registros) |
| **Herramientas**      | Excel + Power Query + Power Pivot + DAX                                    |
| **Elementos clave**   | Modelo relacional, medidas DAX avanzadas, dashboard interactivo  

## 🔴 Objetivo
Este proyecto tiene como objetivo analizar la evolución de las nuevas hipotecas constituidas en España, tanto en número como en importe, desde 2003 hasta 2024. El resultado final es un dashboard interactivo en Excel que permite visualizar tendencias, comparar comunidades autónomas y explorar datos por naturaleza de la finca.

## 👆 Habilidades demostradas
1. **Extracción, Transformación y Carga de datos (ETL)**
2. **Limpieza y validación de datos**
3. **Modelado de datos** (creación de relaciones entre tablas)
4. **Creación de medidas avanzadas con DAX**
5. **Desarrollo de un dashboard interactivo**

## 📖 Fuente de datos
Datos públicos del Instituto Canario de Estadística sobre nuevas hipotecas constituidas según naturaleza de la finca, a nivel de comunidades autónomas y provincias (2003-2024).

[Enlace a los datos](https://datos.canarias.es/catalogos/general/dataset/nuevas-hipotecas-constituidas-segun-naturaleza-de-la-finca-comunidades-autonomas-y-provincias-p)

## 🧵 Proceso detallado

### 1. Preparación de datos
- De los datos originales solamente e seleccionaron las columnas relevantes:

![Tabla de datos general](Imagenes/1imagen.PNG)

  - `MEDIDASHes`: Tipo de dato (número o importe de hipoteca)
  - `TIME_PERIOD#es`: Periodo temporal
  - `FINCA_NATURALEZA#es`: Naturaleza de la finca
  - `TERRITORIO#es`: Ubicación geográfica
  - `OBS_VALUE`: Valor registrado

### 2. Transformación de datos
- Se crearon tres tablas principales:
  1. **Tabla de hechos**: Datos principales de hipotecas
  
  ![Tabla inicial](Imagenes/2imagen.PNG)
  
  2. **Tabla Calendario**: Para análisis temporal avanzado

  ![Tabla Calendario](Imagenes/3imagen.PNG)
  
  3. **Tabla Territorio**: Para organización geográfica
    
  ![Tabla Territorio](Imagenes/4imagen.PNG)
  

### 3. Modelado de datos
- Se establecieron relaciones entre las tablas:
  - Calendario ↔ Tabla de hechos (por fecha)
  - Territorio ↔ Tabla de hechos (por ubicación)
    
  ![Vista de diagrama](Imagenes/5imagen.PNG)
  

### 4. Medidas DAX
- **Medidas básicas**:
  - Total de hipotecas
  - Año máximo/mínimo
- **Medidas avanzadas**:
  - Crecimiento interanual
  - Top 3 comunidades por importe

###  5. Visualización

Podemos visulizar:
- Gráficos combinados (columnas y líneas)
- Tablas dinámicas con formato condicional
- Elementos interactivos:
  - Segmentadores (slicers) por comunidad autónoma y naturaleza de finca
  - Escala de tiempo para filtrar por años
- Elementos dinámicos:
  - Título que se actualiza automáticamente
  - Tarjetas KPI con información relevante
  
  ![Dashboard interactivo de hipotecas en España](Imagenes/6imagen.PNG)

## 🖥 El dashboard permite
- Analizar tendencias temporales
- Comparar comunidades autónomas
- Explorar datos por tipo de propiedad
- Identificar años con mayor actividad hipotecaria

## 🔍 Insights Clave

- Año pico: 2006 (3.7 millones de hipotecas)
- CCAA líderes: Madrid (23%), Cataluña (19%), Andalucía (12%)
- Recuperación: Crecimiento del 15% en importe (2015-2020)

## 🚀 Cómo Usar

- Descargar archivo dashboard_hipotecas.xlsx
- Habilitar contenido si se solicita
- Interactuar con:
  - Filtros superiores (CCAA/tipo propiedad)
  - Selector de rango temporal
  - Tablas dinámicas

## 🔴 Conclusión
Este proyecto demuestra habilidades integrales en el análisis de datos, abarcando desde la extracción hasta la visualización, utilizando herramientas estándar del ecosistema Microsoft.

Si bien el dashboard se ha diseñado de manera sencilla de forma intencionada, ya que plataformas como Power BI o Tableau ofrecen mayores capacidades para crear visualizaciones más atractivas y eficientes, gracias a sus herramientas avanzadas de diseño.
