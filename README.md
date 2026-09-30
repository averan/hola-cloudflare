# hola-cloudflare

Página «Hello World!» en HTML puro (sin build) para probar **Cloudflare Pages**.

```
index.html   Página principal
404.html     Página de error (Cloudflare Pages la usa automáticamente)
_headers     Cabeceras de seguridad (formato de Cloudflare Pages / Netlify)
```

## Ver en local

```bash
python3 -m http.server 5200
```

Abre http://localhost:5200

## Publicar en Cloudflare Pages

1. Entra a https://dash.cloudflare.com (crea una cuenta gratis si no tienes).
2. **Workers & Pages → Create → Pages → Connect to Git**.
3. Autoriza GitHub y elige el repositorio **hola-cloudflare**.
4. Configuración de build:
   - Framework preset: **None**
   - Build command: *(vacío)*
   - Build output directory: `/`
5. **Save and Deploy**. Queda en `https://hola-cloudflare.pages.dev` (o un nombre parecido).

Desde ahí, cada `git push` a `main` se publica solo.
