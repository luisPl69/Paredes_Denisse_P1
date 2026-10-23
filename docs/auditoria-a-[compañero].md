# Informe de Auditoría - Estudiante N.º 21

**Auditor:** Luis Plasencia  
**Auditado:** Estudiante N.º 21 - Taller mecánico

## Hallazgos encontrados

| N.º | Requisito | Ubicación | Hallazgo | Norma que incumple | Severidad |
|-----|-----------|-----------|----------|-------------------|------------|
| 1 | Navegación accesible | `index.html`, línea 18 | El enlace "Saltar al contenido principal" tiene `href="#contenido-principal"`, pero el `<main>` tiene `id="inicio"`. Los nombres no coinciden, el enlace no funciona. | WCAG 2.2, criterio 2.4.1 (Omitir bloques)  | Alta |
| 2 | Formulario accesible | `index.html`, línea 115 | El formulario usa `method="get"`. Como pide datos personales (nombre, teléfono, correo), debería usar `method="post"` para que los datos no aparezcan en la URL. | Especificación HTML WHATWG (atributo `method` del elemento `form`)  | Media |
| 3 | Contraste de colores | `css/estilos.css`, línea 113 (clase `.boton`) | El color `#08717b` con texto blanco tiene contraste de 4.63:1. Pasa el mínimo (4.5:1), pero está muy al límite y podría fallar en algunas pantallas. | WCAG 2.2, criterio 1.4.3 (Contraste mínimo)| Baja |

## Correcciones sugeridas

### Hallazgo 1
**Solución:** Cambiar `href="#contenido-principal"` por `href="#inicio"` en la línea 18, o cambiar el `id="inicio"` del `<main>` por `id="contenido-principal"`.

### Hallazgo 2
**Solución:** Cambiar `method="get"` por `method="post"` en la línea 115.

### Hallazgo 3
**Solución:** Oscurecer el color del botón de `#08717b` a `#076069` para mejorar el contraste a 5.5:1.
