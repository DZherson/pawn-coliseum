# Pawn Coliseum ♟️

Gestor de torneos de ajedrez con emparejamiento por sistema suizo (holandés FIDE)
y round robin, cálculo de rating ELO y desempates oficiales.

🔗 **Demo en vivo:** https://pawn-coliseum.vercel.app

> ⚠️ Proyecto en desarrollo activo. Construido como herramienta real para dirigir
> los torneos del club de ajedrez Ejército de Peones.

## El problema que resuelve

Dirigir un torneo de ajedrez a mano es lento y propenso a errores: emparejar a los
jugadores respetando colores y rivales previos, calcular desempates y actualizar
ratings consume tiempo y abre la puerta a equivocaciones. Pawn Coliseum automatiza
ese proceso aplicando los algoritmos oficiales de la FIDE.

## Características

- Autenticación con roles: administrador, árbitro y jugador.
- Gestión de jugadores con rating ELO.
- Creación y configuración de torneos.
- Emparejamiento automático por sistema suizo holandés (FIDE) y round robin.
- Registro de resultados ronda por ronda.
- Cálculo de rating ELO y desempates (Buchholz, Sonneborn-Berger).
- Perfil público de jugador con historial y evolución de rating.

## Stack tecnológico

- **Frontend:** React 19, TypeScript, Vite 7
- **Estado del servidor:** TanStack Query
- **UI:** Tailwind CSS, shadcn/ui
- **Backend:** Supabase (PostgreSQL, Auth, Row Level Security)
- **Testing:** Vitest, Testing Library, Playwright
- **CI/CD:** GitHub Actions, Vercel

## Cómo ejecutarlo en local

Requisitos: Node.js 24 y una cuenta de Supabase.

```bash
# 1. Clonar el repositorio
git clone https://github.com/DZherson/pawn-coliseum.git
cd pawn-coliseum

# 2. Instalar dependencias
npm install

# 3. Configurar variables de entorno
cp .env.example .env.local
# Edita .env.local con tu URL y anon key de Supabase

# 4. Arrancar el servidor de desarrollo
npm run dev
```

## Scripts disponibles

| Comando | Descripción |
|---|---|
| `npm run dev` | Servidor de desarrollo |
| `npm run build` | Build de producción |
| `npm test` | Ejecuta los tests |
| `npm run lint` | Análisis de código con ESLint |
| `npm run typecheck` | Verificación de tipos |

## Estado del proyecto

- [x] Sprint 0 — Setup, infraestructura, CI/CD y deploy
- [ ] Sprint 1 — Autenticación, roles y gestión de jugadores
- [ ] Sprint 2 — Torneos y emparejamiento round robin
- [ ] Sprint 3 — Sistema suizo FIDE
- [ ] Sprint 4 — Rating ELO, desempates y dashboard
- [ ] Sprint 5 — Pulido y documentación

## Licencia

MIT