# Análisis de una cartera de seguros

**Proyecto de práctica con datos sintéticos** · Python · Pandas · Power BI

Trabajé con un dataset de seguros para entender cómo estaba compuesta la cartera, revisar la calidad de los datos y analizar primas, coberturas, reclamos y renovaciones previstas.

Quise hacer el recorrido completo: empezar por el archivo original, detectar inconsistencias, preparar una base para el análisis, comparar distintos grupos y después organizar los resultados en Power BI.

## Qué trabajé

- **Calidad de datos:** revisé tipos, nulos, duplicados, identificadores y formatos de fecha.
- **Preparación:** separé 2.247 registros con fechas de renovación anteriores al inicio de la póliza.
- **Análisis exploratorio:** comparé tipos de póliza, segmentos, reclamos, canales, productos, regiones y renovaciones.
- **Variables derivadas:** calculé duración de pólizas, agrupaciones por edad y score, y relación cobertura/prima.
- **Visualización:** armé tres vistas en Power BI para presentar los principales indicadores y preguntas de negocio.

## Algunas cifras del análisis

| Indicador | Resultado |
| --- | ---: |
| Registros originales | 53.503 |
| Registros con fechas inconsistentes | 2.247 |
| Registros del análisis principal | 51.256 |
| Registros para el análisis de duración | 51.233 |
| Prima total en el dataset analizado | 154.881.341 |
| Registros señalados para revisar cobertura/prima | 2.563 |

**Qué encontré:** `Group` concentra la mayor prima total entre los tipos de póliza; encontré un grupo de registros con relación cobertura/prima especialmente alta; y observé diferencias entre meses en el volumen de renovaciones previstas. El notebook muestra los cálculos y cómo llegué a esas conclusiones.

## Archivos

- `analisis_seguros_github.ipynb`: exploración, limpieza, análisis y conclusiones.
- `requirements.txt`: dependencia necesaria para ejecutar el notebook.
- `data_synthetic.csv`: archivo de entrada esperado. **No está incluido en esta entrega.** Para reproducir las celdas hay que colocarlo en la misma carpeta, siempre que se tenga derecho a compartir o utilizar ese dataset.

## Cómo ejecutarlo

1. Tener Python y Jupyter (por ejemplo, la extensión Jupyter en VS Code).
2. Instalar la dependencia: `pip install -r requirements.txt`.
3. Colocar el archivo `data_synthetic.csv` junto al notebook.
4. Abrir `analisis_seguros_github.ipynb` y ejecutar las celdas en orden.

El notebook exporta `df_analysis.csv` e `insurance_duration_analysis.csv` para su posterior uso. Las salidas visibles que ya trae son las guardadas durante mi análisis original; no sustituye disponer del CSV de entrada si se quiere reproducir todo.

## Aclaraciones importantes

Este caso está hecho con **datos sintéticos**, no con información de una empresa cliente. Por eso, las conclusiones describen el dataset trabajado y las recomendaciones son posibles líneas de análisis, no mejoras implementadas.

Tampoco interpreto los valores diferentes de `Customer ID` como una cantidad confirmada de clientes únicos. Y los 2.563 registros marcados por una relación cobertura/prima alta son **casos para revisar**, no riesgos ni errores verificados.

## Próximos pasos

La presentación visual del caso incluye tres dashboards de Power BI: resumen ejecutivo, riesgo y oportunidades, y renovaciones y gestión comercial. Cuando esté publicada la página del proyecto en el portfolio, se puede añadir aquí su enlace.
