# 🪟 OptiGlass

**Demo en línea:** https://optiglass.onrender.com

OptiGlass es una aplicación web para optimizar cortes rectangulares sobre láminas de vidrio y otros materiales planos. Calcula distribuciones eficientes, reduce desperdicios y proporciona una visualización gráfica del plano de corte para facilitar la planificación y ejecución de trabajos de corte.

## ✨ Características

- Configuración de ancho, alto, espesor y margen de corte de la lámina.
- Tamaño inicial de lámina de 250 cm × 360 cm.
- Espesores de vidrio por uso: 4 mm, 6 mm, 8 mm y 10 mm o más.
- Registro de múltiples piezas con cantidad, duplicado y eliminación.
- Validaciones para dimensiones, cantidades y piezas que no caben.
- Rotación automática de piezas cuando mejora el acomodo.
- Algoritmo multipasada basado en Guillotine Best Short Side Fit.
- Métricas de aprovechamiento, desperdicio, piezas colocadas y sobrante.
- Plano visual en Canvas con colores, leyenda y marcas de piezas rotadas.
- Exportación del plano como imagen PNG.
- Generación de órdenes de corte en PDF.
- Historial de pedidos.
- Gestión de datos de cliente y notas.
- Cálculo de costos de material y desperdicio.
- Soporte para múltiples láminas.
- Guardado automático del último pedido en el navegador.
- Compatibilidad con modo claro y modo oscuro.

## 🛠 Tecnologías

- HTML5
- CSS3
- JavaScript (Vanilla JS)
- Canvas API
- Flask (opcional para despliegue local)
- LocalStorage

## 📂 Estructura

```text
OptiGlass/
|-- index.html
|-- server.py
|-- requirements.txt
`-- README.md
```

## 🚀 Uso local

### Opción 1: abrir el archivo

Abre `index.html` directamente en un navegador moderno.

### Opción 2: usar Flask

Instala las dependencias:

```bash
pip install -r requirements.txt
```

Ejecuta el servidor:

```bash
python server.py
```

Luego abre:

```text
http://127.0.0.1:5000
```

## 📋 Cómo usar

1. Ingresa las dimensiones de la lámina.
2. Elige el espesor del vidrio.
3. Ajusta el margen de corte (kerf) si es necesario.
4. Agrega las piezas con ancho, alto y cantidad.
5. Haz clic en **Calcular corte óptimo**.
6. Revisa las métricas de aprovechamiento y desperdicio.
7. Analiza el plano visual generado.
8. Exporta el resultado como PNG o PDF si lo deseas.

## 🪟 Espesores

El espesor ajusta el kerf mínimo sugerido y modifica la recomendación de corte.

El kerf (o rodaja) es el espacio que consume la herramienta de corte al atravesar el material. Tenerlo en cuenta evita errores acumulativos en las dimensiones finales de las piezas.

| Espesor | Uso | Kerf mínimo |
|----------|----------|----------|
| 4 mm | Ventanas pequeñas o claraboyas | 2 mm |
| 6 mm | Ventanas residenciales y mesas | 3 mm |
| 8 mm | Puertas de ducha | 4 mm |
| 10 mm o más | Mamparas y divisiones | 5 mm |

## 🧠 Algoritmo

La aplicación utiliza una variante del algoritmo **Guillotine Best Short Side Fit (BSSF)**.

Para mejorar los resultados, OptiGlass evalúa múltiples estrategias de ordenamiento:

- Área descendente.
- Lado mayor.
- Ancho.
- Alto.
- Diferencia entre lados.

En cada intento permite rotación de piezas y conserva la distribución con menor desperdicio encontrada.

El kerf se aplica durante la división de los rectángulos libres para mantener el margen de corte entre piezas.

## 📊 Interpretación de resultados

### ✅ Corte eficiente

Aprovechamiento igual o superior al 85%.

### ⚠️ Corte aceptable

Aprovechamiento entre 65% y 84.9%.

### ❌ Corte ineficiente

Aprovechamiento inferior al 65%.

## 📈 Historial de versiones

### v1.5

- Historial de pedidos.
- Gestión de clientes y notas.
- Exportación de órdenes de corte en PDF.
- Soporte para múltiples láminas.
- Cálculo de costos de material.
- Navegación entre láminas.
- Mejoras generales de estabilidad y experiencia de usuario.

### v1.3

- Canvas de distribución visual ocupa todo el ancho disponible.
- Eliminado el patrón de fondo en el área sobrante.
- Actualización de versión en el footer.

### v1.2

- Selector de espesor con usos recomendados.
- Ajuste automático del kerf mínimo según espesor.
- Tamaño inicial actualizado a 250 cm × 360 cm.
- Visualización de sobrante total y mayor sobrante reutilizable.

### v1.1

- Corrección de textos con codificación incorrecta.
- Renombrado del archivo principal a `index.html`.
- Actualización del servidor Flask.
- Validaciones más estrictas.
- Guardado automático con `localStorage`.
- Botones para cargar ejemplo, limpiar, duplicar piezas y exportar PNG.
- Mejoras de diseño responsive.

## 🎯 Casos de uso

OptiGlass puede utilizarse para:

- Vidrierías.
- Talleres de aluminio y vidrio.
- Fabricación de espejos.
- Corte de acrílico.
- Corte de MDF.
- Corte de láminas metálicas.
- Procesos de manufactura ligera.

## 👨‍💻 Autor

Juan David Vega Alfonso  
Estudiante de Ingeniería de Sistemas.

## 📄 Licencia

MIT License.

Puedes utilizar, modificar y distribuir este proyecto libremente respetando los términos de la licencia MIT.
