# Proyecto Integrador Módulo 4

**Autor:** Juan Sebastian Barreto Benavides  
**Email:** Jsbarreto.sparking@gmail.com  
**Cohorte:** DA-FT13  
**Fecha de entrega:** 12/05/2025  
**Institución:** Farmotudo

---

## 🧠 Introducción

Este proyecto tiene como objetivos principales:

- Aplicar técnicas de carga, filtrado, limpieza y transformación de datos con **Python**, usando las librerías **Pandas** y **NumPy**.
- Aplicar herramientas avanzadas de **estadística** y **visualización de datos**.
- Integrar Python con **Power BI** para importar, analizar y preparar el conjunto de datos en un dashboard interactivo.

---

## 🚧 Desarrollo del Proyecto

### 🔹 Avance 1

1. **Filtrado por país**  
   - Se seleccionaron: Colombia, Argentina, Chile, México, Perú y Brasil.  
   - Se usó `.isin()` para filtrar los países.

2. **Exploración inicial**  
   - Tamaño del dataset antes/después del filtro.  
   - Fechas mínimas y máximas.  
   - Columnas disponibles y tipo de datos de `date`.

3. **Filtrado por fecha**  
   - Se eliminaron registros anteriores al 01/01/2021.

4. **Eliminación de nulos extremos**  
   - Se eliminaron filas y columnas vacías.  
   - Se eliminaron columnas con más de 4 millones de nulos.

5. **Filtrado por códigos de país (`location_key`)**

6. **Limpieza de fechas y nulos**  
   - Conversión a `datetime`.  
   - Relleno con promedio, `ffill` y `bfill`.

7. **Análisis exploratorio (`describe()`, `info()`)**

8. **Selección de columnas clave**  
   - `new_confirmed`, `new_deceased`, `population`, `gdp_usd`, `life_expectancy`.

9. **Guardado del dataset limpio**  
   - Archivo: `DatosFinalesFiltrado.csv`.

10. **Estadísticas descriptivas con bucles**

11. **Función personalizada de estadística**  
   - Calcula media, mediana, varianza y rango.

---

### 🔹 Avance 2

1. **Estadísticas generales por país**  
   - Casos, muertes, vacunación (media, mediana, desviación, mínimo, máximo).

2. **Matriz de correlación**  
   - Variables: casos, muertes, esperanza de vida, diabetes, tabaquismo, etc.

3. **Histogramas de nuevos casos por país**  
   - Observación de distribución y outliers.

---

### 🔹 Avance 3

1. **Verificación de valores nulos**

2. **Resumen por país (últimos valores acumulados)**  
   - Agrupación con `groupby()` y `agg()`.

3. **Cálculo de casos activos estimados**  
   ```python
   data["casos_activos_estimados"] = (
       data["cumulative_confirmed"] -
       data["cumulative_recovered"] -
       data["cumulative_deceased"]
   )
   ```

4. **Visualización**  
   - Gráfico de línea comparando casos activos vs. recuperados (ejemplo: Chile).

5. **Análisis de correlación entre variables**  
   - `sns.heatmap()` con variables relevantes.

6. **Clasificación de nuevos casos según promedio**  
   - Nueva columna: `clasificacion_nuevos_casos`.

7. **Filtrado de casos "Altos"**  
   - Segmentación para análisis específico.

8. **Verificaciones adicionales**  
   - Estructura, valores nulos, frecuencia por país.

---

## 📊 EDA e Insights

- Casos acumulados por país.
- Dosis de vacunas por país.
- Recuperados por país.
- Población de cada país.
- Evolución de casos activos vs. recuperados (ej. Colombia).
- Relación vacunación vs. casos confirmados.
- Promedio de nuevos casos confirmados por país.

---

## 📈 Análisis del Dashboard

- Portada con botón de retorno.
- Gráficos dinámicos.
- graficos con scrip de python
![image](https://github.com/user-attachments/assets/a46531ba-6000-4399-b806-7a603564c077)
- Filtro por países (AR, BR, CL, CO, MX, PE).
- Cambio de visualizaciones según el filtro.
![image-1](https://github.com/user-attachments/assets/91d081f2-097e-4bad-b090-dbe987a00a38)

---

## ✅ Conclusiones y Recomendaciones

- **Brasil** es el país con más casos acumulados.
- **México**, **Argentina** y **Brasil** lideran en vacunación.
- **Brasil** tiene más recuperados: 5,565,456.
- Mayor población: 1° Brasil
- Promedio más alto de casos confirmados: Chile y Argentina.
- Alta demanda de vacunas en Brasil y Mexico.
- Fuerte relación entre vacunación y casos confirmados en Brasil.
- Mayor número de fallecidos: Brasil

---

## 💭 Conclusión Final

Brasil representa una oportunidad estratégica para expansión de empresas farmacéuticas, por su alta población y casos de COVID-19. También se destaca por su sistema de salud activo y la receptividad a la vacunación.

---

## 🙋‍♂️ Reflexión Personal

> A lo largo de este proyecto he aprendido muchísimo. Fue un proceso acelerado en el que tuve que adaptarme rápido, resolver errores y aplicar nuevos conceptos. Me gustaría tener más tiempo para practicar y reforzar lo aprendido, pero reconozco que he avanzado más de lo que imaginaba.
