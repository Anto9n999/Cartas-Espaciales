# PNG de las cartas

Cada carta busca primero su PNG propio y, si no existe, el compartido:

- Combate, propio (opcional): `combat/<id>.png`, p. ej. `combat/caza-tactico.png`, `combat/fragata-pesada.png`.
- Combate, de clase: `combat/caza.png`, `combat/interceptor.png`, `combat/corbeta.png`, `combat/fragata.png`.
- Apoyo, propio (opcional): `support/<id>.png`, p. ej. `support/centro-de-mando.png`.
- Apoyo, compartido por ilustración: `support/logistica.png`, `ingeniera.png`, `escudo.png`, `dron.png`, `laser.png`, `planeta.png`.

Hoy TODAS las cartas tienen su PNG propio, generado con `npm run sprites` (IA local gratuita; ver apuntes/ESTADO.md).
Para sustituir uno por un dibujo propio basta con poner tu PNG con el mismo nombre.

El id es el nombre de la carta en minúsculas, sin tildes y con guiones. Los PNG compartidos (de clase) son
PROVISIONALES y solo se ven si falta el propio (`node scripts/png-provisionales.mjs --forzar` los regenera). Para la versión publicada hay que
volver a ejecutar `npm run build` tras añadir PNG.
