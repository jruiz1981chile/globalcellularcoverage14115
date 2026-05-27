# Global Cellular Coverage

Visualizador interactivo de antenas de telefonia movil a nivel mundial. Muestra celdas cercanas, operadores, tecnologias y diagnostico de cobertura para cualquier punto del planeta usando datos abiertos.

## Caracteristicas

- Busqueda por direccion, pais o punto de interes
- Deteccion de ubicacion por GPS
- Mapa interactivo con celdas geolocalizadas (Leaflet + OpenStreetMap)
- Filtros por tecnologia (GSM, UMTS, LTE, NR/5G) y operador
- Metricas en tiempo real: celdas, operadores, tecnologias detectadas
- Diagnostico de area: mejor operador, distancia minima/promedio, celdas modernas
- Indice de senal calculado localmente
- Referencias globales: nPerf, Ookla 5G Map, Opensignal, GSMA, CellMapper
- Diseno responsive (desktop y movil)
- App Android nativa via Capacitor

## Fuentes de datos

| Fuente | Uso |
|---|---|
| OpenCelliD (CC BY-SA 4.0) | Base de datos de celdas moviles |
| Nominatim / OpenStreetMap | Geocoding de direcciones |
| OpenStreetMap | Mapa base |
| nPerf | Mapa de cobertura crowdsourced |
| Ookla | Mapa 5G global |
| Opensignal | Experiencia movil por mercado |
| GSMA | Referencia global de redes |

## Stack

- HTML/CSS/JS vanilla (single-page app)
- Leaflet 1.9.4 (mapas)
- Capacitor 8.x (wrapper Android)
- @capacitor/geolocation (GPS)

## Desarrollo

```bash
npm install
```

### Web

Abrir `index.html` directamente en el navegador.

### Android

```bash
# Sincronizar web al proyecto Android
npm run build:android

# Abrir en Android Studio
npm run open:android
```

### Generar APK

```powershell
.\build-apk.ps1
```

Requiere Android Studio y Android SDK instalados.

## Estructura

```
├── index.html              # App completa (HTML + CSS + JS)
├── capacitor.config.json   # Config Capacitor
├── package.json
├── build-apk.ps1           # Script para generar APK
├── www/                    # Web assets para Capacitor
└── android/                # Proyecto Android nativo
```

## Licencia

ISC · Datos de OpenCelliD bajo CC BY-SA 4.0 · Mapas OpenStreetMap bajo ODbL
