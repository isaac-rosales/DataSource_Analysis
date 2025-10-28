# 📊 DataSource Analysis – Power BI

## 🔍 Visión General

Este Power BI se conecta a múltiples workspaces y cataloga todos los reportes publicados junto con sus fuentes de datos. Su objetivo principal es proporcionar un **catálogo de datos** para el equipo de visualización, ayudando a comprender las consultas y activos utilizados en los reportes.

## 🧠 Propósito

- Centralizar metadatos sobre informes y conjuntos de datos de Power BI.
- Identificar y clasificar los tipos de fuentes de datos utilizadas.
- Apoyar la gobernanza, documentación y optimización de los flujos de datos.

## 🛠️ Características

- Conexión a múltiples workspaces mediante endpoints XMLA.
- Extracción de metadatos de conjuntos de datos y particiones.
- Limpieza y normalización de consultas M.
- Clasificación de tipos de fuente mediante script en Python.
- Salida estructurada con workspace, reporte, tabla, consulta y tipo de fuente.

## 📁 Flujo de Datos

1. **Conexión a workspaces**  
2. **Extracción de Reportes y Conjuntos de Datos**  
3. **Metadatos de Particiones**  
4. **Ejecución de Script en Python**  
5. **Salida Final**  

## 🧾 Resumen del Código M

La lógica principal está implementada en Power Query (M) e incluye:

- Análisis y limpieza de URLs de workspaces
- Extracción de metadatos usando `AnalysisServices.Database`
- Script en Python para normalización y clasificación
- Formateo final y renombramiento de columnas

## 🐍 Detalles del Script en Python

El script embebido en Python:

- Normaliza cadenas de consulta M.
- Usa expresiones regulares y heurísticas para detectar:
  - SQL, Oracle, KQL, MDX
  - Expresiones DAX
  - JSON, listas o texto codificado
  - Consultas vacías o desconocidas

## 📦 Dependencias

- Power BI Desktop o Servicio con acceso a endpoint XMLA
- Entorno Python habilitado en Power BI
- Librerías requeridas:
  - `pandas`
  - `numpy`

## ⚙️ Recomendaciones de Configuración

- Habilitar el script de Python en Power BI:  
  **Archivo > Opciones y configuración > Opciones > Scripts de Python**

- Activar la opción de privacidad para evitar errores de combinación de datos:  
  **Archivo > Opciones y configuración > Opciones > Privacidad > Ignorar niveles de privacidad**

## 📌 Notas

- Asegúrese de tener permisos de acceso a los espacios de trabajo.
- Este informe está destinado para uso interno del equipo de datos y gobernanza.

## 📄 Licencia

Este proyecto es propietario y está destinado para uso interno dentro de la organización. Contacte al equipo de datos para acceso o colaboración.
