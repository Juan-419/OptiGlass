# 🪟 OptiGlass

**OptiGlass** es una aplicación web desarrollada en HTML, CSS y JavaScript que permite optimizar el corte de piezas rectangulares sobre una lámina de vidrio. Su objetivo es maximizar el aprovechamiento del material, reducir desperdicios y ofrecer una representación visual clara de la distribución de corte.

## ✨ Características

- 📏 Configuración de dimensiones de la lámina de vidrio.
- ✂️ Ajuste del margen de corte (kerf).
- 📦 Gestión de múltiples piezas con cantidades personalizadas.
- 🔄 Rotación automática de piezas para mejorar el ajuste.
- 📊 Cálculo del porcentaje de aprovechamiento.
- 🗑️ Cálculo del porcentaje de desperdicio.
- 🎨 Visualización gráfica del plano de corte.
- 🌙 Compatibilidad con modo claro y modo oscuro.
- ⚡ Funciona completamente en el navegador sin dependencias externas.

---

## 🚀 Tecnologías utilizadas

- HTML5
- CSS3
- JavaScript (Vanilla JS)
- Canvas API

---

## 📋 Cómo usar

1. Ingresa las dimensiones de la lámina disponible.
2. Define el margen de corte (kerf) en milímetros.
3. Agrega las piezas necesarias indicando:
   - Ancho (cm)
   - Alto (cm)
   - Cantidad
4. Haz clic en **"Calcular corte óptimo"**.
5. Revisa los resultados obtenidos:
   - Aprovechamiento de la lámina.
   - Desperdicio estimado.
   - Cantidad de piezas colocadas.
   - Plano visual de distribución.

---

## 🧠 Algoritmo de optimización

OptiGlass utiliza una variante del algoritmo:

### Guillotine Best Short Side Fit (BSSF)

Este algoritmo:

- Ordena las piezas de mayor a menor área.
- Busca el mejor espacio libre para cada pieza.
- Permite rotaciones cuando mejoran el ajuste.
- Divide el espacio restante en nuevos rectángulos libres.

Esto permite obtener distribuciones eficientes en tiempo real para la mayoría de escenarios de corte rectangular.

---

## 📊 Interpretación de resultados

### ✅ Corte óptimo
Aprovechamiento igual o superior al **85%**.

### ⚠️ Corte aceptable
Aprovechamiento entre **65% y 84%**.

### ❌ Corte ineficiente
Aprovechamiento inferior al **65%**.

---

## 🎨 Visualización

El plano de corte muestra:

- Piezas coloreadas según sus dimensiones.
- Etiquetas con las medidas originales.
- Área sobrante resaltada para facilitar su identificación.
- Leyenda automática de piezas utilizadas.

---

## 🛠 Instalación

No requiere instalación.

### Método 1: Uso local

1. Descarga el archivo `index.html`.
2. Ábrelo en cualquier navegador moderno:
   - Google Chrome
   - Microsoft Edge
   - Mozilla Firefox
   - Opera

### Método 2: Publicación web

Puedes alojar el archivo en cualquier servicio de hosting estático como:

- :contentReference[oaicite:0]{index=0}
- :contentReference[oaicite:1]{index=1}
- :contentReference[oaicite:2]{index=2}

---

## 📂 Estructura del proyecto

```text
OptiGlass/
│
├── index.html
└── README.md
```

Todo el proyecto está contenido en un único archivo HTML para facilitar su distribución y mantenimiento.

---

## 🔮 Mejoras futuras

- Soporte para múltiples láminas.
- Exportación a PDF.
- Exportación a imagen PNG.
- Generación de reportes de corte.
- Historial de optimizaciones.
- Gestión de inventario de sobrantes.
- Soporte para materiales distintos al vidrio.
- Optimización avanzada mediante algoritmos evolutivos.

---

## 💡 Casos de uso

OptiGlass puede utilizarse para:

- Vidrierías.
- Talleres de aluminio y vidrio.
- Carpinterías.
- Corte de MDF.
- Corte de acrílico.
- Corte de láminas metálicas.
- Procesos de manufactura ligera.

---

## 👨‍💻 Autor

Juan David Vega Alfonso, estudiante de la universidad catolica del programa de ingenieria de sistemas
Desarrollado como una herramienta práctica para la optimización de cortes rectangulares y el aprovechamiento eficiente de materiales.

---

## 📄 Licencia

MIT License

Puedes usar, modificar, distribuir y adaptar este proyecto libremente, conservando el aviso de licencia correspondiente.
