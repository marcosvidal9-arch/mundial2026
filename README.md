# Mundial 2026 Tracker - V15.2

Versión basada en V15.1 con mejoras de visualización inspiradas en páginas tipo marcador deportivo.

## Cambios principales

- Mejora de tarjetas en el calendario semanal y partidos del día.
- Visualización responsive corregida para computador y celular.
- Etiquetas de fase más claras: grupos, 32avos, 16avos, cuartos, semifinal, tercer lugar y final.
- Resultados mostrados como marcador central, evitando cruces de texto con banderas o ciudades.
- Mantiene `data/results.json` como archivo separado para actualizar resultados desde GitHub.
- Mantiene vista de cruces en lista y bracket visual.

## Actualizar resultados

Editar `data/results.json`:

```json
{
  "1": { "home": 2, "away": 0, "status": "final" },
  "2": { "home": 2, "away": 1, "status": "final" }
}
```

Los resultados con `status: "final"` quedan bloqueados visualmente en la app.

## Uso en GitHub Pages

Subir todos los archivos al repositorio y activar GitHub Pages desde la rama principal.
