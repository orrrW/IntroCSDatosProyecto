# **Impacto de la contaminación por material particulado en la salud respiratoria de los habitantes de Santiago de Chile (2017--2019)**

Este proyecto estudia cómo varían los casos de enfermedades respiratorias en relación con los niveles de contaminación atmosférica
por material particulado fino (PM₂₅) en la Región Metropolitana de Santiago entre 2017 y 2019.

La motivación surge del persistente problema de calidad del aire en Santiago, donde los niveles de PM₂.₅ superan ampliamente los estándares
recomendados por la OMS y se intensifican durante los meses de invierno, coincidiendo con aumentos en enfermedades respiratorias reportados por
la literatura científica y medios nacionales.

## **Objetivo General**

Evaluar la relación temporal entre los niveles de contaminación atmosférica (PM₂₅) y los registros de enfermedades respiratorias en
Santiago, con el fin de identificar patrones estacionales y posibles asociaciones entre ambas variables.

## **Objetivos Específicos**

-   Analizar la evolución mensual de pacientes con enfermedades respiratorias en la RM.
-   Examinar los niveles de PM₂₅ registrados entre 2017 y 2019.
-   Identificar coincidencias temporales entre incrementos de contaminación y aumento de consultas médicas.
-   Explorar diferencias estacionales (invierno vs. verano).

## **Alcance y Ajustes Metodológicos**

El proyecto originalmente incluía variables climáticas (NASA POWER) y socioeconómicas (CASEN). Sin embargo, se descartaron por:

-   **Falta de necesidad real** de la API NASA dado el enfoque final.\
-   **Incompatibilidad y complejidad** del análisis socioeconómico para la escala del proyecto.\
-   **Ausencia de suficientes variables climáticas** en los datasets definitivos.

El análisis se centró exclusivamente en: - **Datos de salud del DEIS (REM)**: número de pacientes por causa respiratoria por comuna y mes.\
- **Datos de contaminación del SINCA**: niveles de PM₂.₅ por estación de monitoreo.

## **Fuentes de Datos Utilizadas**

### **1. DEIS -- Sistema de Reportes REM (MINSAL)**

-   Variables: motivo de consulta, número de pacientes, comuna.\
-   Formato: XLS (estructura HTML).\
-   Cobertura: mensual, 2017--2019.

### **2. SINCA -- Sistema de Información Nacional de Calidad del Aire (MMA)**

-   Variables: fecha, PM₂.₅ validado y preliminar.\
-   Formato: CSV.\
-   Cobertura: estaciones de la Región Metropolitana, 2017--2019.

## **Metodología**

1.  Recolección de datos desde plataformas oficiales.\
2.  Limpieza y estandarización de fechas, comunas y registros numéricos.\
3.  Análisis Exploratorio de Datos (EDA) mediante:
    -   Gráficos de tendencia temporal.
    -   Mapas y visualizaciones geográficas.
    -   Promedios por mes y por comuna.
4.  Comparación temporal entre:
    -   Niveles de PM₂.₅.
    -   Número de pacientes por causas respiratorias.

## **Resultados Principales**

-   Se observa un **aumento simultáneo** de contaminación y casos respiratorios en los meses fríos (mayo--agosto).\
-   El patrón temporal confirma **diferencias estacionales marcadas**, con picos en invierno.\
-   No existe correlación geográfica clara entre comunas con mayor polución y aquellas con mayor número de pacientes.\
-   Las diferencias pueden deberse a:
    -   coberturas desiguales de sensores,
    -   variaciones poblacionales,
    -   causas no ambientales de enfermedades,
    -   desbalance en el tamaño de los conjuntos de datos.

## **Conclusiones**

Los datos muestran una relación estacional clara: los aumentos de PM₂₅ durante el invierno coinciden con incrementos en enfermedades respiratorias. Sin embargo, no se observó una asociación espacial directa entre comunas, posiblemente debido a limitaciones en la cobertura de datos.

## **Estructura del Repositorio**

    IntroCSDatosProyecto/
    ├── 1era Entrega/
    │   └── Informe de Propuesta Inicial
    ├── 2da Entrega/
    │   ├── información y contexto.ipynb
    │   └── relacion_PM_con_mapa_comunas_y_pacientes (unificación).ipynb
    └── README.md
