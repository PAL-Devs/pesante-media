# pesante-media

Imágenes y vídeos publicados en las redes de **Pesante Analytics**.

## Por qué este repo es público

No es un descuido. Instagram no acepta que le subas un archivo: exige una **URL
pública** desde la que sus servidores descarguen la imagen, de forma anónima. Un
repo privado devolvería 404.

Todo lo que hay aquí ya está publicado en Facebook o Instagram. No se pierde
privacidad: se pierde si alguien sube aquí algo que no debía.

## Reglas

**1. Solo entra lo que ya va a ser público.** Imágenes y vídeos destinados a
publicarse. Nunca código, `.env`, tokens, datos de clientes, ni capturas de
informes con cifras reales. El historial de git es público y no se borra de
verdad.

**2. Nombres `AAAA-MM-DD-slug.ext`**, en minúsculas, sin acentos ni espacios.
La fecha delante ordena el repo y permite cruzarlo con los registros de
publicación.

**3. Solo se añade.** No borres ni renombres nada ya publicado: una publicación
de Facebook puede seguir apuntando a esa URL. Si algo sale mal, sube un archivo
nuevo con otro nombre.

**4. Instagram solo acepta JPEG.** El PNG vale para Facebook, no para Instagram.

## Estructura

```
img/    imágenes y vídeos, un archivo por publicación
```

## Cómo se sube

No a mano. Desde el proyecto `AutomatizarDatos`:

```powershell
python scripts\publicar_media.py --archivo contenido\2026-08-11-tema.jpg
```

Ese script comprueba las reglas antes de subir, se niega a sobrescribir un
archivo existente, y verifica que la URL responde de forma anónima antes de darla
por buena.

Las reglas completas y el porqué de cada decisión están en
`AutomatizarDatos/docs/MEDIOS.md` (repo privado).
