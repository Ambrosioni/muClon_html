# ⚔️ MU Online (Season 1/2) — Lorencia Remaster Prototype

> **Experimento de Desarrollo de Videojuego Web 3D en un Solo Archivo**  
> Desarrollado como un prototipo experimental impulsado por **Argon 4.0 (Gemini)**.

Este repositorio contiene un prototipo jugable, autónomo y completamente autocontenido de **MU Online (Season 1 & 2)** ambientado en el clásico mapa de **Lorencia**. El objetivo de este experimento es demostrar la viabilidad de crear una experiencia 3D isométrica completa dentro de un **único archivo HTML**, sin dependencias locales, sin servidores dedicados y sin descargas externas pesadas.

---

## 🌟 Características Principales

### 🗡️ Gráficos 3D Procedurales (Three.js r128)
- **Modelado Procedural sin Assets Externos:** Todos los modelos (Dark Knight, piezas de armadura del Set Dragon y Dark Phoenix, Alas de Dragón, Espadas, Escudos y Criaturas) son generados mediante geometrías paramétricas y texturas procedurales sintetizadas en tiempo de ejecución.
- **Efectos de Brillo Clásicos de MU (+9 a +15):** Pulso senoidal de emisión luminosa y auras doradas que emulan el mítico brillo de las armaduras y armas de MU Online.
- **Física y Animación Dinámica:** Alas con aleteo e inclinación sensibles a la velocidad del héroe, estelas de ataque, partículas de ceniza y viñeta *Dark Fantasy* con niebla exponencial.

### 🌲 Mundo de Lorencia Extendido
- **Recreación Fiel:** Fuente central de regeneración, foso de agua perimetral, 4 puentes de piedra y madera (Norte, Sur, Este y Oeste), antorchas con iluminación cálida y sombras suaves.
- **Árboles Procedurales con Colisión:** Generación de robles oscuros, pinos góticos y ruinas en las afueras con detección de colisiones físicas circulares (`addCircleCollider`) para el jugador y los monstruos.
- **Spots Clásicos de Farmeo (70+ Criaturas):**
  - **Sur (Pantano / Bosque):** Swarms de *Spiders* (Nivel 2).
  - **Este (Planicie / Pradera):** Manadas de *Bull Fighters* (Nivel 6).
  - **Oeste (Ruinas Malditas):** Akelarre de *Liches* con ataque a distancia (Nivel 12).
  - **Norte (Paso Montañoso Helado):** Legión de *Giant Robots* (Nivel 20).
  - **Noreste (Santuario Dorado):** Evento periódico de **Golden Invasion** con el temible *Golden Titan* (Jefe Dorado Nivel 28).

### 📱 Diseño Mobile-First & Controles Táctiles
- **Touch-First Controls:** Toca para moverte o atacar, y mantén presionado para desplazamiento continuo (estilo joystick virtual).
- **Floating Action Pad:** Botones táctiles circulares en la esquina inferior derecha:
  - Botón de **Habilidad Activa** (*Cyclone*, *Twisting Slash*, *Swell Life*, *Rageful Blow*).
  - Botón de **Recolección Rápida** (*Loot / Zen*).
- **HUD Adaptativo:** Interfaz compacta en pantallas móviles (≤ 900px y ≤ 480px), orbes de Vida y Maná escalables, minimapa colapsable con un toque y ventanas modales fluidas con scroll gótico.

### 🛡️ Mecánicas RPG & Persistencia
- **Atributos Clásicos:** Distribución de puntos libres en Fuerza (STR), Agilidad (AGI), Vitalidad (VIT) y Energía (ENE).
- **Economía y Botín:** Drops de Zen, Joyas (*Jewel of Bless*, *Jewel of Soul*) y cajas (*Box of Kundun*).
- **NPCs Funcionales:** Interacción con el *Herrero Han* (Tienda y Forja) y el *Vault Keeper* (Baúl de almacenamiento).
- **Persistencia:** Guardado y carga automática del progreso en el navegador mediante `localStorage`.

---

## 🎮 Controles

### En Dispositivos Móviles / Táctiles:
| Acción | Control |
|---|---|
| **Moverse / Fijar Objetivo** | Tocar en el terreno o sobre una criatura |
| **Caminar Continuo** | Mantener presionado el dedo en la pantalla |
| **Lanzar Habilidad** | Botón flotante dorado de Habilidad |
| **Recoger Botín** | Botón flotante celeste "RECOGER" |
| **Minimizar / Expandir Mapa** | Tocar la barra de título del minimapa |
| **Abrir Menús** | Botones de la barra inferior (C, I, V, Forja) |

### En Computadora / Escritorio:
| Acción | Tecla / Ratón |
|---|---|
| **Moverse / Atacar** | Clic Izquierdo (mantener para continuo) |
| **Ejecutar Habilidad Activa** | Clic Derecho (mantener presionado) |
| **Pociones de Vida / Maná** | <kbd>Q</kbd> / <kbd>W</kbd> |
| **Habilidades (1 a 4)** | <kbd>1</kbd>, <kbd>2</kbd>, <kbd>3</kbd>, <kbd>4</kbd> |
| **Atributos del Personaje** | <kbd>C</kbd> |
| **Inventario y Mochila** | <kbd>I</kbd> |
| **Baúl de Lorencia** | <kbd>V</kbd> |
| **Teletransportarse al Pueblo** | <kbd>M</kbd> |
| **Recoger Zen / Joyas** | <kbd>Espacio</kbd> |
| **Zoom de Cámara** | Rueda del Ratón (Scroll) |

---

## 🚀 Cómo Ejecutar el Proyecto

Este proyecto no requiere Node.js, Webpack, servidores locales ni procesos de compilación:

1. Clona este repositorio o descarga el archivo:
   ```bash
   git clone https://github.com/TU_USUARIO/mu-online-lorencia-remaster.git
   ```
2. Abre directamente el archivo principal en cualquier navegador web moderno (Chrome, Edge, Firefox, Safari o navegadores móviles):
   ```text
   index.html
   ```
3. **GitHub Pages:** Ya está configurado con `index.html` en la raíz, por lo que GitHub Pages cargará el juego automáticamente como página principal.

---

## 🔬 Sobre el Experimento

Este prototipo fue concebido, diseñado y construido como una prueba de concepto experimental asistida por **Argon 4.0 (Gemini)**, explorando hasta qué punto es posible emular la profundidad visual, arquitectura de combate, sistemas de audio Web Audio API procedural y adaptación responsiva de un MMORPG clásico de PC dentro de una única página web ultraligera.

---

## 📜 Licencia

Proyecto creado con fines educativos y de investigación sobre renderizado 3D web y generación procedural.  
*Inspirado en el universo y diseño clásico de MU Online (Webzen).*
