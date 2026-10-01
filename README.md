# bolichapp.com

Sitio estático de BolichApp (GitHub Pages): inicio, aviso de privacidad, condiciones y borrado de
cuenta, en es-MX (`/`) y en inglés (`/en/`). Sin JavaScript, cookies ni recursos externos.

- Repo git propio (remoto `Web-BolichApp`), ubicado en `site/` dentro del repo de la app, que lo
  ignora. Los commits se hacen aquí dentro (`git -C site …`), nunca desde la raíz de la app.
  GitHub Pages publica la raíz de la rama principal.
- `CNAME` = `bolichapp.com`. En DNS: registros `A`/`AAAA` del apex a GitHub Pages y
  `www` → `CNAME` a `<usuario>.github.io`; activar "Enforce HTTPS".
- Las URLs que usa la app están en `src/utils/siteUrls.ts`: si cambia una ruta aquí, cámbiala allá.
- Antes de publicar: `grep -rn TODO site/` debe salir vacío.
- Vista previa local: `python -m http.server -d site 8080` (las rutas son absolutas desde `/`).
