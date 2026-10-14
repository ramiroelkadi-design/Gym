# Mi plan de gym (PWA)

App de seguimiento de entrenamiento: historial por ejercicio, última vez, gráficos de peso y repeticiones, marca "subir peso" y medidas semanales. Es una página estática (sin servidor): los datos se guardan en el navegador del celular.

## Contenido
- `index.html`: toda la app (un solo archivo).
- `manifest.webmanifest`, `sw.js`, `icons/`: lo que la vuelve instalable y usable sin conexión.
- Este paquete trae **solo el plan vacío** (ejercicios, objetivos y semanas). **No incluye tus pesos ni medidas**: van aparte, en el respaldo JSON.

## 1. Subir a GitHub
1. Creá un repositorio nuevo (por ejemplo `gym`).
2. Subí todos los archivos de esta carpeta a la raíz del repositorio (`index.html`, `manifest.webmanifest`, `sw.js`, `LEEME.md` y la carpeta `icons`).
3. En el repositorio: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, rama `main`, carpeta `/ (root)`. Guardá.
4. En uno o dos minutos queda en `https://TU-USUARIO.github.io/gym/`.

En cuentas gratuitas Pages necesita repositorio público. Como acá no hay datos personales, no pasa nada.

## 2. Pasar lo que ya cargaste
1. Abrí la URL de GitHub Pages en Chrome del celular.
2. Pestaña **Datos → Importar respaldo** y elegí `respaldo-gym-2026-10-13.json`.
3. Confirmá. Quedan todos tus entrenamientos, notas, marcas de "subir peso" y medidas.

El archivo de respaldo tiene tus datos: guardalo en tu Drive o en el celular, **no lo subas al repositorio**.

## 3. Instalarla
En Chrome: menú ⋮ → **Instalar app** (o "Agregar a la pantalla principal"). Se abre como app y funciona sin internet.

## Cosas a tener en cuenta
- Los datos viven en ese navegador y en ese dominio. Si cambiás de celular o borrás los datos del navegador, se pierden: usá **Datos → Exportar respaldo** de vez en cuando (por ejemplo una vez por semana).
- Para pasar los datos a otro dispositivo: exportás el respaldo en uno e importás en el otro.
- Las copias de la app publicada en Claude y la de GitHub son independientes. Una vez que importes el respaldo, usá solo una para no duplicar cargas.
- Para actualizar la app, reemplazá `index.html` en el repositorio. El celular toma la versión nueva al abrirla con conexión. Tus datos no se tocan. Si cambiás otros archivos, subí también el número de `VERSION` en `sw.js`.
