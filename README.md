# Aprendizaje Colaborativo y Práctico – 2do Parcial  
## Suite CAAT (1–5) + Modo libre

Esta aplicación en **Streamlit** implementa una **suite de herramientas CAAT (Computer Assisted Audit Techniques)** orientadas a la auditoría asistida por computadora.  
Permite analizar datos cargados en formato **CSV o XLSX**, detectar irregularidades y generar reportes descargables en **CSV**.

---

## 🚀 Funcionalidades principales

- ✔ Robustez de cargas: acepta **CSV/XLSX** (requiere `openpyxl`).  
- ✔ Archivos se mantienen en memoria (cache en sesión).  
- ✔ Autodetección de columnas y opción de selección manual.  
- ✔ Claves únicas en widgets (evita `StreamlitDuplicateElementId`).  
- ✔ Reportes CSV descargables en todos los módulos.  
- ✔ Indicadores KPI y visualizaciones simples.  
- ✔ Incluye un **Modo libre (EDA)** para explorar cualquier dataset.

---

## 📦 Requisitos

- Python 3.9+  
- Librerías:  
  ```bash
  pip install streamlit pandas numpy openpyxl
  ```

---

## ▶️ Ejecución

1. Clona este repositorio o descarga los archivos.  
2. Instala dependencias:  
   ```bash
   pip install -r requirements.txt
   ```
3. Ejecuta la aplicación:  
   ```bash
   streamlit run app.py
   ```
4. Abre en el navegador la URL local que muestra Streamlit (ej. `http://localhost:8501`).

---

## 🛠️ Módulos incluidos

### **CAAT 1 – Registros fuera de horario**  
- Detecta actividades realizadas fuera del rango laboral definido.  
- Permite configurar inicio/fin de jornada y opción de solo días hábiles.  
- Exporta hallazgos y ranking de reincidentes.

### **CAAT 2 – Auditoría de privilegios (roles críticos y SoD)**  
- Analiza usuarios y roles.  
- Marca **roles críticos** de forma automática o manual.  
- Permite definir **reglas SoD** (`ROL_A -> ROL_B`) para detectar conflictos.  
- Descarga listas de conflictos y roles críticos.

### **CAAT 3 – Conciliación de logs vs transacciones**  
- Cruza **logs** y **transacciones** por ID y fecha.  
- Identifica **faltantes** y **fuera de tolerancia (minutos)**.  
- Opción adicional: **conciliación bancaria** (extracto vs libro).  

### **CAAT 4 – Variación inusual de pagos (outliers)**  
- Analiza pagos históricos por proveedor.  
- Aplica **z-score robusto (MAD)** para detectar outliers.  
- Umbral ajustable y exportación de resultados.

### **CAAT 5 – Duplicados / near-duplicados**  
- Detecta duplicados exactos en columnas clave.  
- Identifica near-duplicados (mismo monto y fechas cercanas).  
- Descarga CSV de hallazgos.

### **Modo libre – EDA guiado**  
- Explora cualquier dataset (CSV/XLSX).  
- Muestra KPIs rápidos (conteo, nulos, suma, promedio, etc.).  
- Incluye filtros dinámicos y descarga de datos filtrados.

---

## 📊 Conclusión sugerida

- Priorizar **concentración de outliers** (CAAT 4),  
  **reincidencia fuera de horario** (CAAT 1),  
  y **conflictos SoD** (CAAT 2).  
- En conciliación (CAAT 3), enfocar en los **gaps de tolerancia** y registros **no conciliados**.  
- Descargar CSVs generados para documentar evidencias.

---

## 📄 Licencia

Uso académico – Proyecto universitario de **Auditoría de Sistemas y Bases de Datos**.
