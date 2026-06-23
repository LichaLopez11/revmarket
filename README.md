# RevMarket ⚙️

**E-Commerce de repuestos, accesorios y partes de autos.**

> Actividad Formativa N.º 2 — Algoritmos y Estructuras de Datos 2026  
> UTN Facultad Regional Resistencia

---

## 🌐 Aplicación

👉 [Ver RevMarket en vivo](https://lichalopez11.github.io/revmarket/)

La app permite explorar un catálogo de repuestos con buscador por descripción o vehículo compatible, y filtros por categoría y estado de la pieza.

---

## 📦 Entregables

| Archivo | Descripción |
|---|---|
| `index.html` | Aplicación web generada con IA (Claude Opus) |
| `registro.docx` | Diseño del registro principal con clave correspondiente |

---

## 🗂️ Registro Principal

El registro principal del sistema es `PUBLICACION`, que modela cada producto publicado en la plataforma.

```
PUBLICACION = Registro
    IdPublicacion:     N(6);
    CodParte:          AN(20);
    Descripcion:       AN(100);
    Categoria:         AN(30);
    MarcaParte:        AN(30);
    MarcaVehiculo:     AN(30);
    ModeloVehiculo:    AN(30);
    AnioDesde:         N(4);
    AnioHasta:         N(4);
    Estado:            AN(15);
    Precio:            R(10);
    Stock:             N(4);
    FechaPublicacion = Registro
        Dia:   N(2);
        Mes:   N(2);
        Anio:  N(4);
    Fin Registro;
    IdVendedor:        N(6);
Fin Registro;
```

**Clave primaria:** `IdPublicacion` — identifica de forma única cada publicación.  
**Clave secundaria:** `Categoria` — permite ordenar y filtrar por rubro.  
**Campo continente:** `FechaPublicacion` — compuesto por `Dia`, `Mes` y `Anio`.

---

## 🤖 Prompts utilizados

### Prompt 1 — Generación de la app
> Quiero que me ayudes a crear una aplicación web llamada **RevMarket**, un e-Commerce de compra y venta de repuestos, accesorios y partes de autos. Diseño automotriz/industrial: fondo oscuro (negro o gris muy oscuro), detalles en naranja, tipografía moderna y robusta.
>
> Generá una aplicación web completa en un único archivo HTML con CSS y JavaScript embebidos. Debe incluir:
> - Header con nombre "RevMarket" y slogan breve
> - Catálogo con al menos 6 publicaciones de ejemplo con datos reales y variados: repuestos de distintas categorías (motor, suspensión, frenos, carrocería, electrónica), distintas marcas de autos (Ford, Volkswagen, Toyota, Chevrolet), distintos estados (Nuevo, Usado, Reacondicionado) y precios en pesos argentinos formateados (ejemplo: $125.000)
> - Cada tarjeta de producto debe mostrar: descripción, categoría, marca del repuesto, vehículo compatible con año, estado y precio
> - Buscador funcional por descripción o vehículo compatible
> - Filtros funcionales por categoría y por estado
> - Sección "Sobre RevMarket" con descripción breve del negocio
> - Footer con nombre del proyecto
> - Diseño responsive
>
> El código debe quedar limpio y listo para subir como `index.html` a GitHub Pages.

### Prompt 2 — Pulido final
> Revisá el HTML completo que generaste y corregí lo siguiente si hace falta:
> 1. Que el buscador y los filtros funcionen correctamente en JavaScript sin errores
> 2. Que la paleta de colores y tipografía sean consistentes en toda la página
> 3. Que todos los precios estén formateados en pesos argentinos con puntos de miles (ejemplo: $125.000)
> 4. Que el diseño sea responsive y se vea bien en celular
> 5. Que el código esté limpio, sin comentarios innecesarios y listo para producción
>
> Entregame el archivo HTML final completo.

---

## 🛠️ Herramienta utilizada

[Claude](https://claude.ai) — Anthropic
