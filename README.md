# Mundial 2026 Tracker - V15 Data Driven

Versión basada en V14 pública, pero con resultados centralizados en `data/results.json`.

## Cómo actualizar resultados globalmente

1. Entra al repositorio de GitHub.
2. Abre el archivo `data/results.json`.
3. Edita o agrega el resultado usando el ID del partido.
4. Guarda el cambio con Commit.
5. GitHub Pages mostrará los resultados actualizados al recargar.

Ejemplo:

```json
{
  "1": { "home": 2, "away": 0, "status": "final" },
  "2": { "home": 2, "away": 1, "status": "final" }
}
```

## Cómo identificar el ID

En la app cada partido tiene su número de match. Ese número es la clave usada en `results.json`.

- Match 1: México vs Sudáfrica
- Match 2: Corea del Sur vs Chequia

## Fase eliminatoria con empate

Si un partido de eliminación directa termina empatado y clasifica alguien por alargue o penales, agrega `winner`:

```json
{
  "89": { "home": 1, "away": 1, "winner": "home", "method": "penales", "status": "final" }
}
```

Valores posibles para `winner`:
- `home`: clasifica el equipo local de esa tarjeta
- `away`: clasifica el equipo visitante de esa tarjeta

## Nota local

Al abrir el HTML con doble clic, algunos navegadores bloquean `fetch` de archivos JSON. Para probar la actualización real, súbelo a GitHub Pages o ejecútalo con un servidor local simple:

```bash
python -m http.server
```
