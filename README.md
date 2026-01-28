# 📦 Sistema de Gestión de Inventarios (Simulador Pro v3.2)

![Version](https://img.shields.io/badge/version-3.2.0-blue?style=for-the-badge&logo=appveyor)
![Estado](https://img.shields.io/badge/estado-Estable-success?style=for-the-badge)
![Licencia](https://img.shields.io/badge/licencia-MIT-orange?style=for-the-badge)
![Developer](https://img.shields.io/badge/developer-Juancito_Peña-red?style=for-the-badge)

> Un generador de datos masivos y simulador de inventarios inteligente, capaz de crear miles de transacciones realistas, calcular KPIs financieros y exportar reportes mensuales automatizados.

---

## 📑 Tabla de Contenidos
1. [Introducción](#-introducción)
2. [Planteamiento del Problema](#-planteamiento-del-problema)
3. [Solución Propuesta](#-solución-propuesta)
4. [Tecnologías Utilizadas](#-tecnologías)
5. [Características Principales](#-características-principales)
6. [Instalación y Uso](#-instalación-y-uso)
7. [Autor y Contacto](#-autor)
8. [Contribuir y Apoyar](#-contribuir)

---

## 🚀 Introducción

Este proyecto es una herramienta web *Client-Side* (se ejecuta 100% en el navegador) diseñada para **Analistas de Datos, Gerentes de Inventario y Desarrolladores**. Permite simular un entorno empresarial complejo con múltiples regiones, gerentes y turnos, generando data histórica coherente para pruebas de estrés, dashboards de Excel/Power BI o entrenamiento de modelos de datos.

---

## 🧐 Planteamiento del Problema

En el mundo del análisis de datos y el desarrollo de software, nos enfrentamos constantemente a estos desafíos:

*   ❌ **Falta de Datos Realistas:** Los datasets de prueba suelen ser planos o aleatorios sin lógica de negocio.
*   ❌ **Cálculos Manuales Tediosos:** Calcular rotación, días de inventario y vencimientos para miles de registros toma horas.
*   ❌ **Estructura Plana:** La mayoría de generadores no consideran jerarquías (Región > Gerente > Encargado > Turno).
*   ❌ **Exportación Limitada:** Separar manualmente un archivo gigante de un año en reportes mensuales es ineficiente.

---

## 💡 Solución Propuesta

El **Sistema de Gestión de Inventarios v3.2** automatiza todo el flujo:

1.  **Lógica de Negocio Probabilística:** Aplica reglas estrictas (73% Excelente, 15% Óptimo, etc.) para simular la realidad operativa.
2.  **Vencimientos Inteligentes:** Calcula la fecha de caducidad basada en la vida útil real del producto (ej. La leche vence rápido, el arroz no).
3.  **Cálculo de KPIs en Tiempo Real:** Rotación (%), Días de Inventario, Valor de Stock y Condición del producto.
4.  **Exportación Inteligente:** Con un solo clic, el sistema detecta los meses generados y descarga **archivos individuales por mes** (CSV, Excel o JSON).

---

## 🛠 Tecnologías

Este proyecto ha sido construido con tecnologías modernas y ligeras para asegurar compatibilidad y velocidad.

| Tecnología | Uso | Logo |
| :--- | :--- | :--- |
| **HTML5** | Estructura Semántica | <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg" width="25"> |
| **CSS3** | Estilos (Dark Mode) | <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg" width="25"> |
| **JavaScript** | Lógica de Simulación | <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" width="25"> |
| **Bootstrap 5** | Diseño Responsivo y UI | <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bootstrap/bootstrap-original.svg" width="25"> |
| **SheetJS** | Exportación Excel/CSV | <img src="https://cdn.sheetjs.com/sheetjs.png" width="35"> |

---

## 🌟 Características Principales

### 📊 Lógica de Inventario
El algoritmo asegura que la distribución de los datos cumpla con:
*   🟢 **73%** Inventario Excelente.
*   🔵 **15%** Inventario Óptimo.
*   🟡 **10%** Alerta / Poco Inventario.
*   🔴 **<2%** Inventario Negativo (Errores operativos simulados).

### 📅 Vencimientos Realistas
Cada producto tiene una propiedad de `vida_util`. El sistema calcula:
*   **Buen Estado (80%):** Producto fresco.
*   **Cercano a Vencer (10%):** En sus últimos días de vida útil.
*   **Vencido (5%):** Caducado en almacén.
*   **Defectuoso (5%):** Devoluciones o daños.

### 🏢 Estructura Organizacional
Simulación completa de la jerarquía empresarial:
*   **4 Regiones:** Norte, Sur, Este, Cibao.
*   **Gerentes:** Únicos por región.
*   **Encargados:** 3 perfiles diferentes por región.
*   **Turnos:** Mañana, Tarde y Noche (8 horas).

### 💾 Exportación Multi-Archivo
No más archivos gigantes. El sistema:
1.  Agrupa la data por `YYYY-MM`.
2.  Genera un archivo independiente por cada mes.
3.  Soporta formatos `.xlsx` (Excel), `.csv` y `.json`.

---

## 🖥️ Instalación y Uso

No requiere instalación de servidores ni Node.js. Es una aplicación **Plug & Play**.

1.  **Descargar:** Clona este repositorio o descarga el archivo `.html`.
    ```bash
    git clone https://github.com/TU_USUARIO/inventario-generator.git
    ```
2.  **Ejecutar:** Haz doble clic en el archivo `index.html`. Se abrirá en tu navegador predeterminado.
3.  **Configurar:**
    *   Ingresa la cantidad de transacciones (ej. 5000).
    *   Define el rango de fechas (Inicio y Fin).
4.  **Generar:** Presiona el botón **"Generar Data"**.
5.  **Exportar:** Elige tu formato favorito (Excel, CSV o JSON) y el navegador descargará los archivos mensuales automáticamente.

---

## 👨‍💻 Autor

<div align="center">
  <img src="https://avatars.githubusercontent.com/u/38921558?v=4" width="120" style="border-radius: 50%; border: 4px solid #007bff;">
  
  ### **Juancito Peña**
  *Full Stack Developer • Data Scientist • Educator*
  
  <p>Ingeniero en Sistemas apasionado por la automatización de datos, la Inteligencia Artificial y la enseñanza técnica.</p>

  [![YouTube](https://img.shields.io/badge/YouTube-Ver_Canal-red?style=for-the-badge&logo=youtube)](https://www.youtube.com/@JuancitoDevV)
  [![LinkedIn](https://img.shields.io/badge/LinkedIn-Conectar-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/juancitope%C3%B1a/)
  [![GitHub](https://img.shields.io/badge/GitHub-Ver_Repos-black?style=for-the-badge&logo=github)](https://github.com/JUANCITOPENA)
</div>

---

## ⭐ Contribuir

¡Tu apoyo es fundamental! Si este proyecto te ha servido para tus tareas, estudios o trabajo, por favor considera:

1.  **Darle una estrella (⭐)** a este repositorio. ¡Ayuda a que más gente lo encuentre!
2.  **Compartirlo** en tus redes sociales (LinkedIn, Twitter).
3.  **Hacer un Fork** y sugerir mejoras mediante Pull Requests.

---

<p align="center">
  Hecho con ❤️ y mucho código por <strong>Juancito Peña</strong>.
  <br>
  &copy; 2024 - Todos los derechos reservados.
</p>
