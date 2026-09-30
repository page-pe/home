# Page.pe

Sitio web de Page.pe: creación de páginas web para comercios y particulares en Perú.

## Propósito

Generar ingresos mediante la creación de páginas web. Estrategia en dos fases:

### Fase 1 — Landing de servicio (actual)
`www.page.pe` funciona como carta de presentación que respalda la venta
presencial (comercio por comercio). Debe incluir:

- [x] Hero / propuesta de valor
- [x] Qué cambia con una web
- [x] Cómo funciona (proceso en pasos)
- [x] Planes y precios
- [x] Portafolio de sitios trabajados
- [x] Preguntas frecuentes
- [x] Contacto / cotización

### Fase 2 — Editor self-service (futuro)
Los usuarios ingresan a la web, crean y publican su página por sí mismos
(modalidad SaaS, como Wix).

- [ ] Definir stack (editor, auth, pagos, hosting de sitios)
- [ ] Validar con demanda real recolectada en Fase 1

## Estructura

Multipágina: `index.html` corto con el mensaje principal, el detalle en
subpáginas.

- `index.html` — hero, qué cambia, cómo funciona, CTA
- `planes/` — 4 planes con detalle y tabla comparativa
- `portafolio/` — trabajos entregados
- `contacto/` — datos, qué necesitamos saber y FAQ

## Planes

| Plan | Precio | Hosting luego |
| --- | --- | --- |
| Básico | S/ 300 – 800 | S/ 30/mes |
| Profesional | S/ 800 – 1 500 | S/ 60/mes |
| Premium | S/ 1 500 – 3 000 | S/ 120/mes |
| Personalizado | A cotizar | A cotizar |

Todos incluyen 3 meses de hosting gratis. El hosting va aparte y sin
permanencia. El precio es por la web completa, en un solo pago. Dirección
`*.page.pe` incluida; dominio propio (.com) desde el plan Profesional.

## SEO: copy propio, specs compartidas

`www.page.pe` y `page.djc.pe` son dos sitios distintos que deben sumar
tráfico, no canibalizarse. Regla:

- **Copy y ángulo propios.** No se reutiliza el texto del otro sitio. El
  ángulo de `page.pe` es la pérdida por no tener web ("te buscan y no te
  encuentran"), no el proceso de trabajo.
- **Specs técnicas idénticas.** Precios, hosting, features por plan,
  WhatsApp y casos reales son los mismos datos. Eso no es contenido
  duplicado, es información consistente.

## Trazabilidad de WhatsApp

El sitio es estático, sin backend, así que el origen del lead se registra
con el prefill de `wa.me`. Cada botón precarga una consulta redactada como
la escribiría una persona, más una firma de origen en la segunda línea:

```
Hola, quiero cotizar el plan Profesional.
(via page.pe/planes / Profesional)
```

La firma va al final y es breve a propósito: el cliente no debe ver algo
que parece un código de rastreo, pero tú tienes que poder ubicar el lead
de un vistazo. Como `page.pe` y `page.djc.pe` comparten el mismo número,
el prefijo `page.pe` es lo que los distingue.

Al agregar un botón nuevo hay que incluir su firma. El formato es
`?text=<mensaje>%0A%28via%20<origen>%29`, con el texto URL-encoded.
Ojo: en PowerShell 5.1 los `.ps1` se leen como ANSI, así que hay que
generar los acentos desde codepoints Unicode o sale doble encoding
(`%C3%83%C2%A1`) y el cliente recibe el texto roto.

## Decisiones abiertas

- Contexto de venta: visita presencial + landing como respaldo
- Método de contacto: WhatsApp (+51 994 444 789)
- Marca: Page.pe. No se referencian otros productos del ecosistema
- Pendiente: revisar los precios cuando se ajusten los rangos
- Pendiente: más casos reales en el portafolio a medida que se entreguen

## Streaming de trabajo (obligatorio)

- Todo trabajo se hace en una **rama nueva** (nunca directo en `main`).
- Todos los commits de ese trabajo se hacen en esa rama.
- `main` solo recibe cambios por **merge/pull request** cuando el usuario lo autoriza.

## Stack

- HTML/CSS estático en GitHub Pages
- Dominio: `www.page.pe` (CNAME)