# Betómetro · Tienda

Herramientas que se instalan en el Betómetro (Raspberry Pi) desde el botón **Tienda**.

- Cada herramienta es un programa Qt para la Pi, en su carpeta (`brujula/`, `calculadora/`…).
- `tienda.json` es el catálogo: lo que la Pi muestra en la Tienda.
- GitHub arma el paquete de cada herramienta (`nombre-X.Y.Z.tar.gz`) y lo sube como release.

## Cómo funciona en la Pi
1. La Tienda baja `tienda.json` por wifi y muestra cada herramienta en un cuadradito.
2. **Instalar**: baja el paquete del release, comprueba el `sha256` del catálogo y lo guarda en la Pi.
3. **Abrir**: Betómetro se cierra y se abre la herramienta. Al salir, o si se traba, **Betómetro vuelve solo**.
4. Con una carrera en curso no se abre nada.

## El catálogo (`tienda.json`)
```json
{
  "formato": 1,
  "herramientas": [
    {
      "id": "brujula",
      "nombre": "Brújula",
      "descripcion": "Hacia dónde vas, con el GPS",
      "version": "1.0.0",
      "icono": "brujula/icono.png",
      "paquete": "https://github.com/tvmaty2186/Betometro-tienda/releases/download/brujula-1.0.0/brujula-1.0.0.tar.gz",
      "sha256": "…",
      "betometroMinimo": "1.0.35"
    }
  ]
}
```

El programa Betómetro está en [tvmaty2186/Betometro-Raspberry](https://github.com/tvmaty2186/Betometro-Raspberry).
