# Gohan Bestia — tema para Kino TV

Tema de toda la app (apiVersion 18) con estética oscura violeta, aura eléctrica,
bordes finos y logo vectorial propio. Es un plugin **solo de datos**: sin código,
sin red, sin capacidades y con `"hosts": []`.

## Requisitos
- Kino **0.9.81** o posterior (`apiVersion: 18`). Los bordes (`*Border`, `colors.border`) se ven desde Kino 0.9.82; en 0.9.81 se ignoran.

## Instalación
1. Sube esta carpeta a un repositorio de GitHub (`kino-plugin.json`, `plugin.js`, `icon.png`).
2. En Kino: **Ajustes ▸ Plugins ▸ Instalar** y escribe `usuario/repositorio`.
3. Ve a **Ajustes ▸ Apariencia**, elige **Gohan Bestia** y toca **Usar este tema**.
4. Kino preguntará si quieres la experiencia completa (el tema se ve mejor así). Acepta.

## Qué cambia
| Elemento | Valor |
|---|---|
| Acento | `#9B5CFF` (violeta), texto sobre acento `#0B0614` |
| Fondo | Degradado `#0B0614 → #1A0B33 → #0B0614` |
| Esquinas | Más rectas (8–12 dp; 6 dp en TV) |
| Bordes | Diálogos 2 dp; menús, cabeceras, tarjetas y paneles 1 dp |
| Reproductor | Botones redondeados, play ×1.2, barra ×1.2 |
| Movimiento | Zoom de foco 1.08, fundido 250 ms |
| Logo | Rayo + «GOHAN» en vectores (menú, cabecera y riel del TV); marca con aura y rayo para el riel cerrado |
| Icono | `icon.png` (256×256), vinculado en `kino-plugin.json` → `"icon": "icon.png"` |

## Ajustable por la persona
Ajustes ▸ Apariencia ▸ Personalizar: color de acento (5 muestras, aptas para control remoto),
redondeo de tarjetas, escala del texto, grosor de la barra de progreso y fondo.

## Legibilidad
Todos los pares respetan los umbrales de Kino (texto 4,5:1 y UI 3:1):
acento sobre fondo ≈ 5:1, `onAccent` sobre acento ≈ 5:1, fondo oscuro (luminancia < 0,05).

## Probar con el kit
```
node sdk/validate.mjs .
```
No debería mostrar advertencias de celular ni de TV.

## Sobre el logo e icono
El logo y el icono son **diseños vectoriales originales** (rayo y aura) inspirados en la
temática; no reproducen el arte oficial del personaje. Si quieres afinarlos:
- Logo: edita `appThemes[0].logo` (máx. 8 paths, `d` ≤ 2000 caracteres, `fill`: `accent`, `onAccent`, `textPrimary`, `textSecondary` o `#RRGGBB`).
- Icono: PNG cuadrado ≤ 128 KB; la ruta va sin `./`.

## Notas
- No cambies el `id` del tema (`gohan-bestia`) después de publicar: de él cuelgan las elecciones de la gente.
- Desactivar o quitar el plugin devuelve el tema original de Kino.
- Dragon Ball y sus personajes pertenecen a sus respectivos titulares; este tema es un proyecto de fans sin afiliación.
