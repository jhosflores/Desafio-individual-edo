# Simulación de población y capacidad de un refugio animal

Aplicación educativa para estudiar cómo cambia la población de un refugio comunitario mediante una ecuación diferencial ordinaria de primer orden y comparar sus aproximaciones numéricas.

## Problema

El refugio necesita anticipar la cantidad de animales que tendrá que atender para planificar espacio, alimento y campañas de adopción. La aplicación permite explorar escenarios hipotéticos y observar si la población estimada supera una capacidad de referencia `C`.

## Modelo matemático

La población `y(t)` se modela mediante:

`dy/dt = R - k y`, con `y(0) = y₀`.

- `t`: tiempo en semanas.
- `y(t)`: cantidad de mascotas en el refugio.
- `y₀`: población inicial, en mascotas.
- `R`: ingreso constante, en mascotas por semana.
- `k`: tasa proporcional de adopción, en semana⁻¹.
- `C`: capacidad de referencia del refugio, en mascotas. Se usa para evaluar la meta; no forma parte de la ecuación diferencial.

La solución analítica es `y(t) = R/k + (y₀ - R/k)e^(-kt)` y el equilibrio es `R/k`. La aplicación compara esta solución exacta con el método de Heun (RK2) y Runge-Kutta clásico de cuarto orden (RK4), muestra errores, tabla y gráfica, y permite comparar dos tamaños de paso.

Los valores iniciales son hipotéticos y se pueden cambiar en la página. El modelo supone tasas constantes y no incorpora cambios estacionales ni datos observados; sus resultados son escenarios de estudio, no predicciones comprobadas.

## Cómo ejecutar

1. Descarga o clona este repositorio.
2. Abre `index.html` en un navegador actualizado.
3. Ingresa los parámetros y pulsa **Ejecutar y Guardar**.

La página carga Tailwind CSS, Font Awesome, Chart.js y MathJax desde CDN, por lo que se requiere conexión a Internet para que todos los estilos, gráficos y fórmulas se muestren correctamente.

## Publicar con GitHub Pages

1. Sube `index.html` y este `README.md` a la raíz de un repositorio de GitHub.
2. En el repositorio, abre **Settings → Pages**.
3. En **Build and deployment**, selecciona **Deploy from a branch**, elige la rama `main` y la carpeta `/ (root)`, y guarda.
4. Cuando GitHub Pages termine de publicar, copia la URL que aparece en esa misma sección.
