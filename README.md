# 🪟 Optimizador de Corte de Vidrio

Aplicación web desarrollada en HTML, CSS y JavaScript para calcular la distribución de piezas rectangulares dentro de una lámina de vidrio, maximizando el aprovechamiento del material y minimizando el desperdicio.

## 📋 Características

- Definición de dimensiones de la lámina de vidrio.
- Configuración del margen de corte (kerf).
- Agregar múltiples piezas con diferentes dimensiones y cantidades.
- Rotación automática de piezas cuando sea posible.
- Cálculo del porcentaje de aprovechamiento.
- Cálculo del porcentaje de desperdicio.
- Visualización gráfica de la distribución de corte.
- Indicadores de eficiencia del corte.
- Compatibilidad con modo claro y modo oscuro.
- No requiere instalación ni dependencias externas.

---

## 🚀 Tecnologías utilizadas

- HTML5
- CSS3
- JavaScript (Vanilla JS)
- Canvas API

---

## ⚙️ Funcionamiento

1. Ingresa el ancho y alto de la lámina disponible.
2. Define el grosor del corte (kerf) en milímetros.
3. Agrega las piezas necesarias indicando:
   - Ancho
   - Alto
   - Cantidad
4. Haz clic en **"Calcular corte óptimo"**.
5. La aplicación mostrará:
   - Aprovechamiento de la lámina.
   - Desperdicio estimado.
   - Número de piezas colocadas.
   - Distribución visual del corte.

---

## 📊 Algoritmo utilizado

La aplicación utiliza una variante del algoritmo:

**Guillotine Best Short Side Fit (BSSF)**

Este método:

- Ordena las piezas por área descendente.
- Busca el mejor espacio disponible para cada pieza.
- Permite rotaciones cuando mejoran el ajuste.
- Divide el espacio restante en nuevos rectángulos libres.

El algoritmo ofrece resultados rápidos y eficientes para la mayoría de escenarios de corte rectangular.

---

## 📸 Vista previa

La aplicación genera una representación visual donde:

- Cada color representa un tipo de pieza.
- Las etiquetas muestran las dimensiones originales.
- El área amarilla representa el material sobrante.

---

## 📈 Interpretación de resultados

### ✅ Corte óptimo

Aprovechamiento igual o superior al 85%.

### ⚠ Corte aceptable

Aprovechamiento entre 65% y 84%.

### ❌ Corte ineficiente

Aprovechamiento inferior al 65%.

---

## 🛠 Instalación

No se requiere instalación.

1. Descarga el archivo HTML.
2. Ábrelo en cualquier navegador moderno:
   - Google Chrome
   - Microsoft Edge
   - Mozilla Firefox
   - Opera

---

## 📂 Estructura del proyecto

```text
/
└── index.html
```

Todo el proyecto se encuentra contenido en un único archivo.

---

## 🔮 Posibles mejoras futuras

- Soporte para múltiples láminas.
- Exportación a PDF.
- Exportación a imagen PNG.
- Generación de reportes de corte.
- Optimización avanzada mediante algoritmos genéticos.
- Gestión de inventario de sobrantes.
- Soporte para materiales distintos al vidrio.

---

## 👨‍💻 Autor

Desarrollado como herramienta de optimización para procesos de corte de vidrio y materiales rectangulares.

---

## 📄 Licencia

Este proyecto puede utilizarse, modificarse y distribuirse libremente para fines educativos y comerciales.
