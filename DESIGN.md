# Especificación de diseño — App de inventario
Estilo: minimalista, blanco y negro, dashboard SaaS moderno (referencia: ui-skills.com)

Fuente base para toda la interfaz: **Inter / SF Pro / system-ui** (sans-serif). No se usa ninguna otra familia tipográfica en ningún componente. (font-family: Inter, "SF Pro", system-ui, sans-serif;)

---

## 1. Logo (sidebar, esquina superior)

| Propiedad | Valor |
|---|---|
| Contenedor del ícono | 26px × 26px, radio de borde 7px |
| Fondo del contenedor | `#0A0A0A` (negro) |
| Ícono dentro | Tabler `ti-cube`, 16px, color `#FFFFFF` |
| Texto del nombre (marca) | 14px, peso 500, color `#0A0A0A` |
| Espacio entre ícono y texto | 8px |
| Distancia al borde superior del sidebar | 20px |

---

## 2. Sidebar (navegación lateral)

| Propiedad | Valor |
|---|---|
| Ancho total | 200–220px, alto 100% |
| Fondo | `#FFFFFF` |
| Borde | 0.5px sólido `#E5E4E0`, solo lado derecho |
| Padding interno | 20px vertical, 16px horizontal |
| Distancia entre secciones (logo / nav / usuario) | 24px |

**Ítem de navegación:**
| Propiedad | Valor |
|---|---|
| Alto | 36px (padding 8px 10px) |
| Tipografía | 13px |
| Peso — inactivo | 400, color `#5F5E5A` |
| Peso — activo | 500, color `#0A0A0A` |
| Fondo — inactivo | transparente |
| Fondo — activo | `#F2F2F0`, radio 8px |
| Ícono | Tabler outline, 16px, mismo color que el texto |
| Espacio ícono–texto | 10px |
| Espacio entre ítems | 2px |

**Bloque de usuario (pie del sidebar):**
| Propiedad | Valor |
|---|---|
| Avatar | círculo 28px × 28px, fondo `#F2F2F0`, iniciales 12px/500 centradas |
| Nombre | 12px, peso 500, color `#0A0A0A` |
| Rol/subtítulo | 11px, peso 400, color `#888780` |
| Separador superior | borde 0.5px `#E5E4E0`, padding-top 16px |

---

## 3. Header de página (parte superior del contenido)

| Elemento | Tipografía | Color | Notas |
|---|---|---|---|
| Título de página (ej. "Inventario") | 16–18px, peso 500 | `#0A0A0A` | — |
| Subtítulo (ej. "Actualizado hace 4 min") | 12px, peso 400 | `#888780` | debajo del título, sin margen extra |

**Buscador (input de búsqueda en header):**
| Propiedad | Valor |
|---|---|
| Alto | 32px |
| Padding | 6px 10px |
| Borde | 0.5px `#E5E4E0`, radio 8px |
| Ícono | `ti-search`, 14px, color `#888780` |
| Texto placeholder | 12px, color `#888780` |
| Ancho | 200–240px |

---

## 4. Botones

Todos los botones: alto **36px**, radio **8px**, tipografía **13px / peso 500**, sin sombra.

| Tipo | Fondo | Texto/ícono | Borde | Uso |
|---|---|---|---|---|
| **Primario** | `#0A0A0A` sólido | `#FFFFFF` | ninguno | "Agregar", "Guardar cambios" |
| **Secundario / neutro** | transparente | `#0A0A0A` | 0.5px `#E5E4E0` | "Cancelar", "Cerrar" |
| **Destructivo** | `#791F1F` sólido | `#FFFFFF` | ninguno | "Eliminar" (solo en modal de confirmación) |

| Propiedad | Valor |
|---|---|
| Padding horizontal | 12–14px |
| Espacio ícono–texto | 4–6px |
| Tamaño de ícono dentro del botón | 14px |

---

## 5. Inputs (campos de texto, select)

| Propiedad | Valor |
|---|---|
| Alto | 36px |
| Ancho | 100% del contenedor padre |
| Padding | 8px 10px |
| Borde | 0.5px sólido `#E5E4E0`, radio 8px |
| Borde en focus | 1px `#0A0A0A` (sin glow ni sombra) |
| Fondo | `#FFFFFF` |
| Tipografía del valor | 13px, peso 400, color `#0A0A0A` |
| Tipografía placeholder | 13px, peso 400, color `#888780` |
| Label encima del input | 12px, peso 400, color `#5F5E5A`, margen inferior 4px |
| Espacio vertical entre campos apilados | 10px |

`select` (dropdown) usa exactamente las mismas medidas que el input de texto.

---

## 6. Tarjetas de métricas (stat cards)

| Propiedad | Valor |
|---|---|
| Grid | 4 columnas iguales, gap 12px |
| Fondo | `#F2F2F0` |
| Borde | ninguno |
| Radio de borde | 12px |
| Padding interno | 16px |
| Label (ej. "Total productos") | 12px, peso 400, color `#5F5E5A`, margen inferior 6px |
| Número principal | 22–24px, peso 500, color `#0A0A0A` |

---

## 7. Tabla de inventario

| Propiedad | Valor |
|---|---|
| Contenedor | borde 0.5px `#E5E4E0` en todo el perímetro, radio 12px, sin sombra |
| Columnas (grid) | `2fr 1fr 1fr 1fr 1fr 1fr` (Producto, Categoría, Cantidad, Precio, Estado, Acciones) |
| Encabezado de columna | 11px, peso 400, color `#888780`, padding 10px 14px, borde inferior 0.5px |
| Fila | alto ~44px (padding 10px vertical, 14px horizontal), tipografía 13px/400 |
| Separador entre filas | borde inferior 0.5px `#E5E4E0` (nunca líneas verticales) |
| Ícono junto al nombre de producto | Tabler outline, 16px, color `#5F5E5A` |
| Espacio ícono–nombre | 8px |

**Badge de estado (dentro de la columna Estado):**
| Propiedad | Valor |
|---|---|
| Forma | pill, radio 20px (full) |
| Padding | 3px 8px |
| Tipografía | 11px, peso 400 |
| Ícono interno | 12px |
| Disponible | fondo `#EAF3DE`, texto/ícono `#27500A` |
| Bajo stock | fondo `#FAEEDA`, texto/ícono `#854F0B` |
| Agotado | fondo `#FCEBEB`, texto/ícono `#791F1F` |

**Columna Acciones:**
| Propiedad | Valor |
|---|---|
| Íconos | `ti-eye` (ver), `ti-edit` (actualizar), `ti-trash` (eliminar) |
| Tamaño | 16px |
| Espacio entre íconos | 6px |
| Color — ver/actualizar | `#5F5E5A` |
| Color — eliminar | `#791F1F` |
| Cursor | pointer, con `aria-label` obligatorio |

---

## 8. Ventanas emergentes (modales)

| Propiedad | Valor |
|---|---|
| Overlay de fondo | `rgba(0,0,0,0.45)`, cubre toda la pantalla |
| Contenedor del modal | ancho 320–380px, fondo `#FFFFFF`, borde 0.5px `#E5E4E0`, radio 12px, padding 20px |
| Título del modal | 15px, peso 500, color `#0A0A0A` |
| Ícono de cerrar (`ti-x`) | 16px, color `#888780`, esquina superior derecha |
| Espacio entre título y contenido | 14px |
| Espacio entre contenido y botones | 16px |
| Alineación de botones | derecha, gap 8px |

**Variantes por tipo de modal:**

| Modal | Contenido interno | Botón principal |
|---|---|---|
| Agregar | Inputs vacíos (nombre, categoría, precio, cantidad) — ver sección 5 | Primario negro, ícono `ti-plus`, "Agregar" |
| Ver | Ícono 44×44px + nombre (14px/500) + categoría (12px/muted) arriba; tabla de datos abajo (13px, filas de 5px padding vertical) | Secundario "Cerrar" |
| Actualizar | Mismos inputs que Agregar, precargados + `select` de estado | Primario negro, ícono `ti-check`, "Guardar cambios" |
| Eliminar | Ícono `ti-alert-triangle` en círculo 36px fondo `#FCEBEB`/ícono `#791F1F` + texto de confirmación 13px/`#5F5E5A` | Destructivo rojo, ícono `ti-trash`, "Eliminar" |

---

## 9. Iconografía general

| Propiedad | Valor |
|---|---|
| Librería | Tabler Icons, únicamente estilo **outline** |
| Tamaño en tablas/texto en línea | 16px |
| Tamaño en encabezados de tarjeta/modal | 18–20px |
| Tamaño decorativo máximo | 24px |
| Color por defecto | hereda del texto (gris `#5F5E5A`) |
| Color en acciones destructivas | `#791F1F` |

---

## 10. Escala tipográfica resumen (para referencia rápida)

| Tamaño | Peso | Dónde se usa |
|---|---|---|
| 11px | 400 | encabezados de columna de tabla, texto de badges |
| 12px | 400 | labels de input, subtítulos, texto muted, rol de usuario |
| 13px | 400 | texto de tabla, valores de input, texto de confirmación en modales |
| 13px | 500 | texto de botones |
| 14px | 500 | nombre de marca (logo), nombre de producto en modal "ver" |
| 15px | 500 | título de modal |
| 16–18px | 500 | título de página |
| 22–24px | 500 | número principal en stat card |

**Nunca usar:** negrita fuerte (600/700+), cursiva, subrayado, MAYÚSCULAS sostenidas, ni una segunda familia tipográfica.

---

## 11. Principios generales

1. Sin gradientes, sombras decorativas ni efectos de neón/blur — superficies planas.
2. Bordes finos de 0.5–1px en vez de sombras para separar elementos.
3. Un solo acento por vista: el botón negro sólido es la única acción "primaria" visible.
4. El color siempre comunica significado (verde = ok, ámbar = alerta, rojo = crítico), nunca decoración.
5. Espaciado generoso — densidad media-baja, nunca saturar la interfaz.