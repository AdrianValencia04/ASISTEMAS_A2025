# Aprendizaje Colaborativo y Práctico – 2do Parcial
Suite CAAT (1–5) + Modo libre

## 🚀 ¿Qué incluye?
- 5 módulos CAAT listos para usar (fuera de horario, privilegios, conciliaciones, outliers y duplicados).
- Cargas robustas CSV/XLSX (openpyxl), conservación en sesión y descargas XLSX de hallazgos.
- KPIs rápidos y ayudas guiadas por módulo.
- Modo libre para explorar cualquier dataset.

## 📦 Requisitos
```
pip install -r requirements.txt
```

## ▶️ Ejecutar localmente
```
streamlit run app.py
```
La app abrirá en `http://localhost:8501/`.

## 🧩 Módulos
1. **CAAT 1 – Registros fuera de horario**: Define jornada (08:00–17:30 por defecto), días hábiles y opcionalmente cruza **dispositivo** y **ubicación** para inconsistencias.
2. **CAAT 2 – Privilegios y SoD**: Marca **roles críticos** y construye **reglas de segregación de funciones** (ROL_A → ROL_B). Exporta conflictos.
3. **CAAT 3 – Conciliación**: Une **Logs vs Transacciones** por ID y fecha/hora con **tolerancia (min)**. Incluye una **conciliación bancaria simple** por monto y fecha.
4. **CAAT 4 – Outliers de pagos**: Detección por **z-score robusto** configurable.
5. **CAAT 5 – Duplicados**: Exactos por columnas clave y **near-duplicados** por **mismo monto** y **fecha cercana (±días)**.

## 🛠 Consejos
- Prefiere archivos `.xlsx` no protegidos. Revisa el formato de fechas antes de subir.
- Si una columna no se detecta automáticamente, selecciónala manualmente en el selector.
- Todos los hallazgos son descargables como **XLSX** para tus papeles de trabajo.

## ☁️ Despliegue rápido (Streamlit Community Cloud)
1. Sube este repo a GitHub.
2. En **streamlit.io → Deploy**, apunta a `app.py`.
3. Añade los **secrets** que necesites (no requeridos por defecto).

---
© 2025 – Proyecto académico. Uso con fines educativos.
