# FatigaMonitor Pro

Sistema integral de monitorización de la fatiga y del entrenamiento para atletas, desarrollado como Trabajo de Fin de Grado (TFG) por Julián Orejas González — *Monitorización de la fatiga en el alto rendimiento*.

## Descripción

Single Page Application (SPA) empaquetada en un único archivo HTML. Combina planificación del entrenamiento, control del progreso, nutrición personalizada, evaluación antropométrica y monitorización de la fatiga basada en CMJ, wellness score y carga semanal.

## Funcionalidades principales

- **Gestión de atletas**: registro, foto de perfil, ficha detallada con avatar.
- **Dashboard del entrenador**: panel de control con resumen de atletas y alertas de fatiga.
- **Macrociclo / Mesociclo / Microciclo**: planificación anual completa con distribución de carga 0-25, tipos de microciclo (General, Competición, Choque, Activación, Restablecimiento, Competición) y semáforo CMJ basado en MDC (Claudino et al. 2017).
- **Control del progreso**: seguimiento de ejercicios objetivo (press banca, sentadilla, peso muerto, CMJ) con evolución en gráficas.
- **Evaluación antropométrica**: 12 evaluaciones mensuales con mediciones corporales (peso, % grasa, % masa muscular, perímetros).
- **Monitorización CMJ**: gráficas con baseline, tendencia de 8 semanas, % de cambio vs baseline.
- **Wellness score** y **carga semanal** con correlación.
- **Calculadora APRE** (Autoregulated Progressive Resistance Exercise) con 4 protocolos.
- **Módulo de nutrición completo**:
  - BMR con Mifflin-St Jeor o Harris-Benedict.
  - Objetivos personalizables (déficit, mantenimiento, superávit).
  - Panel SMAE (Sistema Mexicano de Alimentos Equivalentes) con 16 grupos y algoritmo dinámico de asignación.
  - Generador de menús semanales (4–6 comidas/día) con filtrado de alergias y scoring de repeticiones.
  - Lista de compras automática con categorización (proteínas / carbohidratos / grasas / verduras y frutas / otros).
  - Exportación a PDF de menú semanal + lista de compras.
- **Informes nutricionales** guardables y exportables.
- **Diseño responsive** y tema visual coherente (paleta neutra con acentos de semáforo).

## Tecnología

- **HTML5 + CSS3 + JavaScript vanilla** (ES6+) — sin framework.
- **Chart.js** (CDN) para gráficas.
- **Font Awesome** (CDN) para iconos.
- **Google Fonts** (Cormorant Garamond, DM Sans, DM Mono, Inter).
- **Persistencia**: `localStorage` del navegador (sin backend).
- **Todo en un solo archivo**: `index.html` (~490 KB, ~7300 líneas).

## Cómo ejecutar

No requiere servidor, instalación ni build. Basta con:

1. Clonar o descargar el repositorio.
2. Abrir `index.html` en cualquier navegador moderno (Chrome, Edge, Firefox, Safari).

Alternativamente, puedes servirlo con cualquier servidor estático:

```bash
# Python 3
python -m http.server 3000

# Node.js
npx serve .
```

Y abrir `http://localhost:3000`.

## Enlace en vivo

🔗 **https://julianog2004-del.github.io/FatigaMonitor/**

Cualquier persona con el enlace puede acceder directamente, registrarse con cualquiera de las 3 cuentas de entrenador (o crear su propio atleta) y todos sus datos se guardarán en el `localStorage` de su propio navegador. Cada dispositivo/navegador tiene su propia copia independiente de los datos.

## Usuarios de prueba

### Entrenadores (contraseña común: `coach123`)

| Entrenador | Email | Atleta asignado |
|---|---|---|
| Julián Orejas | `coach1@fatiga.es` | Carlos Martínez — Entrenamiento de Fuerza |
| Marta Ruiz | `coach2@fatiga.es` | Ana García — Powerlifting |
| Alex Pérez | `coach3@fatiga.es` | Diego López — CrossFit |

Cada entrenador ve **solo sus propios atletas** y puede crear nuevos atletas, planes, mesociclos, informes nutricionales y menús semanales. Todos los datos que crees quedan asociados a tu cuenta de entrenador y se guardan automáticamente en el navegador.

### Atletas (contraseña común: `atleta123`)

- `carlos@fatiga.es` — Carlos Martínez (atleta de coach1)
- `ana@fatiga.es` — Ana García (atleta de coach2)
- `diego@fatiga.es` — Diego López (atleta de coach3)

## Créditos

Trabajo de Fin de Grado — Universidad de Granada (UGR), curso 2025-2026.

**Autor**: Julián Orejas González
