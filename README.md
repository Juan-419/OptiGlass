# OptiGlass

OptiGlass es una aplicacion web para optimizar cortes rectangulares sobre una lamina de vidrio u otros materiales planos. Permite registrar piezas con cantidades, calcular una distribucion de corte y visualizar el aprovechamiento del material en un plano interactivo.

## Caracteristicas

- Configuracion de ancho, alto, espesor y margen de corte de la lamina.
- Tamano inicial de lamina de 250 cm x 360 cm.
- Espesores de vidrio por uso: 4 mm, 6 mm, 8 mm y 10 mm o mas.
- Registro de multiples piezas con cantidad, duplicado y eliminacion.
- Validaciones para dimensiones, cantidades y piezas que no caben.
- Rotacion automatica de piezas cuando mejora el acomodo.
- Algoritmo multipasada basado en Guillotine Best Short Side Fit.
- Metricas de aprovechamiento, desperdicio, piezas colocadas y sobrante.
- Plano visual en Canvas con colores, leyenda y marcas de piezas rotadas.
- Exportacion del plano como imagen PNG.
- Guardado automatico del ultimo pedido en el navegador.
- Compatibilidad con modo claro y modo oscuro.

## Estructura

```text
OptiGlass/
|-- index.html
|-- server.py
|-- requirements.txt
`-- README.md
```

## Uso local

### Opcion 1: abrir el archivo

Abre `index.html` directamente en un navegador moderno.

### Opcion 2: usar Flask

Instala dependencias:

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

## Como usar

1. Ingresa las dimensiones de la lamina.
2. Elige el espesor del vidrio.
3. Ajusta el margen de corte o kerf en milimetros si necesitas cambiar el sugerido.
4. Agrega las piezas con ancho, alto y cantidad.
5. Haz clic en `Calcular corte optimo`.
6. Revisa las metricas, el plano de corte y la leyenda.
7. Usa `Exportar PNG` para guardar el plano.

## Espesores

El espesor ajusta el kerf minimo sugerido y cambia la recomendacion de corte.

El kerf (o rodaja) es el espacio que consume el disco o rueda de corte al pasar sobre el vidrio. Si no se tiene en cuenta, las piezas pueden salir ligeramente mas pequeñas de lo pedido y el error se acumula en cortes consecutivos.

| Espesor | Uso | Kerf minimo |
| --- | --- | --- |
| 4 mm | Ventanas pequenas o claraboyas | 2 mm |
| 6 mm | Ventanas de viviendas y mesas | 3 mm |
| 8 mm | Puertas de ducha | 4 mm |
| 10 mm o mas | Mamparas y divisiones de oficina | 5 mm |

## Algoritmo

La aplicacion usa una variante del algoritmo Guillotine Best Short Side Fit. Para mejorar el resultado, prueba varias ordenaciones de piezas: area, lado mayor, ancho, alto y diferencia entre lados. En cada intento permite rotacion y conserva la mejor distribucion encontrada.

El kerf se aplica como separacion entre cortes al dividir los rectangulos libres. Esto evita rechazar piezas que caben justo en el borde de la lamina, pero mantiene espacio para el margen de corte entre piezas.

## Interpretacion

- Corte eficiente: aprovechamiento igual o superior al 85%.
- Corte aceptable: aprovechamiento entre 65% y 84.9%.
- Corte ineficiente: aprovechamiento inferior al 65%.

## Mejoras incluidas en v1.3

- Canvas de distribucion visual ocupa todo el ancho del panel.
- Eliminado el fondo de patron en el area sobrante del plano de corte.
- Version actualizada en el footer de la aplicacion.

## Mejoras incluidas en v1.2

- Selector de espesor con usos recomendados.
- Ajuste automatico del kerf minimo segun espesor.
- Tamano inicial actualizado a 250 cm x 360 cm.
- Visualizacion de sobrante total y mayor sobrante reutilizable.

## Mejoras incluidas en v1.1

- Correccion de textos con codificacion rota.
- Renombrado del archivo principal a `index.html`.
- Actualizacion del servidor Flask.
- Validaciones mas estrictas.
- Guardado automatico con `localStorage`.
- Botones para cargar ejemplo, limpiar, duplicar piezas y exportar PNG.
- Visualizacion mas legible y responsive.

## Autor

Juan David Vega Alfonso, estudiante de Ingenieria de Sistemas.

## Licencia

MIT License.