# Terry's · Update (chequeos del local)

La página que queda abierta en el iPad del local: **https://update.terrysburgers.com/**

Tres solapas:

- **Ruleta** — canjear códigos y toda la información de los que participaron (por canjear, canjeados, jugadas, jugadores y, para el admin, el QR del flyer).
- **Reservas** — las reservas de la web de los próximos 30 días. Solo para mirar.
- **Cierre de caja** — arqueo por billetes y monedas (apertura / cierre de cada turno) y la planilla con todos los arqueos.

Es un solo archivo, `index.html`. Entra el usuario de **caja** o un **admin** (los mismos de la ruleta, lista `premios_staff`); caja no ve los datos de contacto de los clientes.

## De dónde salen los datos

Del mismo proyecto de Supabase que la ruleta y Administración. Todo pasa por funciones `chequeos_…` de la base; el SQL que las crea está en el repo de la ruleta (`terrys-premios`, archivo `chequeos.sql`), porque usa sus tablas y su lista de usuarios.

## Probar sin base

`index.html?demo` (como caja) o `index.html?demo=admin`: usa datos de ejemplo guardados en el navegador.

## Publicación

GitHub Pages desde la rama `main`. Dominio propio: registro CNAME `update` → `jetraverso.github.io` en el DNS de terrysburgers.com, más el archivo `CNAME` en este repo.
