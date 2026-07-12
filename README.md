# Flujo · Finanzas para negocios pequeños

App web de control de ingresos y gastos para negocios pequeños. Bilingüe (español/inglés), funciona en celular y computadora, sin instalación.

## Direcciones

| Qué | Dirección |
|---|---|
| **Página pública (landing)** | https://appflujo.vercel.app |
| **La app** | https://appflujo.vercel.app/app.html |
| Dirección anterior (sigue activa) | https://flujo-ten-wine.vercel.app |
| Repositorio GitHub | https://github.com/ulichstefano/flujo |
| Panel de Vercel | https://vercel.com/flujoapp/flujo |

## Archivos

- `index.html` — página de inicio comercial (landing) con precios
- `app.html` — la aplicación de finanzas
- `flujo-icon.png` — icono para instalar en el celular

## Cómo funciona el despliegue

Cada cambio se sube así (Claude lo hace automáticamente al pedírselo):

```
git add .
git commit -m "descripción del cambio"
git push
```

Vercel detecta el push y actualiza https://appflujo.vercel.app solo, en menos de 1 minuto.

## Datos técnicos

- Los datos del usuario se guardan en su propio dispositivo (localStorage del navegador), claves: `flujo_records_v1`, `flujo_settings_v1`, `flujo_quick_v1`, `flujo_dark`
- Sin servidor ni base de datos (por ahora)
- Cuenta de Vercel y GitHub: ulichstefano (login con GitHub)
- La app de Vercel en GitHub tiene acceso SOLO al repositorio `flujo`

## Plan de fases

- [x] **Fase 1** — App gratis + landing publicadas (11/07/2026)
- [x] **Fase 2** — Cuentas de usuario y sincronización en la nube con Supabase (11/07/2026)
  - Proyecto Supabase: APPFLUJO (https://kwvwkbluwytizlzhjnew.supabase.co, región us-west-2)
  - Tablas `records` y `user_settings` con seguridad por usuario (RLS)
  - Registro sin confirmación de correo (decisión: menos fricción)
- [ ] **Fase 3** — Suscripción Pro $4.99/mes con Stripe

## Ideas pendientes

- Dominio propio (ej. flujoapp.com, ~$10/año) — más profesional para monetizar
- `flujo.vercel.app` y `flujoapp.vercel.app` están ocupados por otros usuarios
