# Geometry Dash Webport Archive

Archivo del webport WASM de Geometry Dash (`gd_web` build).

## Archivos

| Archivo | Tamaño | Descripcion |
|---|---|---|
| `gd_web.js` | 1.2 MB | Loader Emscripten (glue code) |
| `gd_web.wasm` | 66.6 MB | Binario WebAssembly del juego |
| `gd_web.data` | 300 MB | Assets (musica MP3, texturas, niveles) |
| `ref/` | 2.2 MB | Imagenes de UI (logo, fondo, load) |
| `index.html` | 38 KB | Pagina de inicio con loader |

## Ejecutar localmente

```bash
# Servir con cualquier web server estático (requiere HTTP, no file://)
python -m http.server 8080
# Abrir http://localhost:8080
```

## Detalles tecnicos

- **Emscripten**: Version moderna con Asyncify, WebGL2, IDBFS
- **WebAssembly**: Binario valido (magic 0x0061736d, version 1)
- **Assets**: Formato Emscripten data package (cabecera ID3/MP3 detectada)
- **SHA256 data**: `97046fc16efe6b5c5acbcfbb75886d0164ea11612cdffc8809f121ffb3866536`

## Fuente

CDN original: `cdn.jsdelivr.net/gh/AlexBoops/geo@main/`

## Creditos

Webport creado por **bog** (`<3`). Hosteado en itch.io por **theblehlollipop**.
