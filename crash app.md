# Dashboard Crash Apps
Este panel de Dynatrace es una **vista integral de la estabilidad y rendimiento de las aplicaciones móviles**, enfocado específicamente en la monitorización de **crashes (fallos de la aplicación)** para un conjunto de aplicaciones mobiles de su ambiente.

<img width="1714" height="857" alt="Image" src="https://github.com/user-attachments/assets/62438cc0-346d-48e2-860b-6f396877ba3b" />

## 🛠️ Instrucciones de Instalación del Dashboard

Siga estos sencillos pasos para importar el dashboard a su entorno Dynatrace:

---

### 1. Descarga del Archivo de Configuración

Descargue la definición del dashboard en formato **JSON** desde este repositorio.

* **Archivo:** `crash_apps_dashboard_v1.0.json`
* **Enlace de Descarga:** [**Descargar JSON**]([Insertar el enlace directo al archivo JSON aquí])

---

### 2. Importación en Dynatrace

Una vez que haya descargado el archivo JSON, siga estos pasos dentro de la interfaz de Dynatrace:

1.  Diríjase al menú principal de Dynatrace y seleccione **`Dashboards`** (Paneles de control).
2.  En la parte superior derecha de la pantalla de Dashboards, busque y haga clic en el botón **`Upload dashboard`** (Cargar panel).
    > **Tip Alternativo:** Puede ir a `Settings` (Configuración) > `Dashboards` > `Upload dashboard`.
3.  Se abrirá una ventana de diálogo. Haga clic en **`Browse`** o **arrastre y suelte** el archivo `crash_apps_dashboard_v1.0.json` que descargó en el paso anterior.
4.  El dashboard aparecerá inmediatamente en su lista de paneles y estará listo para ser utilizado.

---

**Nota:** Asegúrese de que su usuario de Dynatrace tenga los permisos necesarios para configurar o cargar nuevos paneles.

Aquí tienes una descripción general de lo que muestra:

## 📊 Descripción General del Panel

El dashboard ofrece una combinación de métricas de alto nivel y detalles granulares para la gestión de fallos de la aplicación:

1.  **Métricas de Alto Nivel:**
    * Muestra el **rendimiento general** (`Apdex`) y el volumen total de **`Sesiones`**.
    * El KPI clave es el **`Free-crash User`** , indicando la proporción de usuarios que no experimentaron fallos, lo que es el indicador directo de la estabilidad.
    * Muestra el **volumen total de `Crash`y su tendencia de cambio.

2.  **Análisis por Plataforma y Tendencias:**
    * Proporciona desgloses claros de los crashes y usuarios afectados por **sistema operativo (`iOS` y `Android`)**.
    * Incluye gráficos de series de tiempo para visualizar la **tendencia de crashes** en Android e iOS, permitiendo identificar picos o la efectividad de las correcciones recientes.

3.  **Diagnóstico Detallado (Punto Crítico):**
    * En la parte inferior, se encuentran las tablas de **`Detalle Crash Android`** y **`Detalle Crash iOS`**, que son cruciales para la resolución de problemas.
    * Estas tablas identifican los **`Nombre Crash`** (por ejemplo, `java.lang.NullPointerException`, `EXC_BREAKPOINT`) que están ocurriendo con mayor frecuencia.
    * Permiten correlacionar la cantidad de ocurrencias y los usuarios afectados con la **`Versión App`** específica, facilitando la identificación de versiones defectuosas que deben ser priorizadas para un parche.

En resumen, es un panel diseñado para que los equipos de ingeniería y producto puedan **evaluar rápidamente la salud de la aplicación**, **cuantificar el impacto de los fallos** en los usuarios y **navegar directamente a la causa raíz** (App Version y Nombre Crash) de los problemas más frecuentes.
