# Page.pe

Sitio web de Page.pe: creación de páginas web para comercios y particulares en Perú.

## Propósito

Generar ingresos mediante la creación de páginas web. Estrategia en dos fases:

### Fase 1 — Landing de servicio (actual)
`www.page.pe` funciona como carta de presentación que respalda la venta
presencial (comercio por comercio). Debe incluir:

- [ ] Hero / propuesta de valor
- [ ] Planes y precios
- [ ] Portafolio de sitios trabajados
- [ ] Contacto / cotización

### Fase 2 — Editor self-service (futuro)
Los usuarios ingresan a la web, crean y publican su página por sí mismos
(modalidad SaaS, como Wix).

- [ ] Definir stack (editor, auth, pagos, hosting de sitios)
- [ ] Validar con demanda real recolectada en Fase 1

## Decisiones abiertas

- Contexto de venta: visita presencial + landing como respaldo
- Estructura de la landing: múltiples páginas
  (`index.html`, `planes.html`, `portafolio.html`, `contacto.html`)
- Método de contacto: WhatsApp (+51 994 444 789)
- Planes y precios: tentativos (Básico / Profesional / Premium), sujetos a ajuste

## Streaming de trabajo (obligatorio)

- Todo trabajo se hace en una **rama nueva** (nunca directo en `main`).
- Todos los commits de ese trabajo se hacen en esa rama.
- `main` solo recibe cambios por **merge/pull request** cuando el usuario lo autoriza.

## Stack

- HTML/CSS estático en GitHub Pages
- Dominio: `www.page.pe` (CNAME)