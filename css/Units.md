
# CSS Units Guide

## Tipos de Unidades

En CSS, las unidades se dividen en dos categorÃ­as principales:

### Unidades Absolutas
- **`px` (pÃ­xeles)**: La Ãºnica unidad absoluta que no cambia. Ãštil para elementos con tamaÃ±os fijos.

### Unidades Relativas
Dependientes de otras variables como:
- **`rem` y `em`**: Relativas al tamaÃ±o de fuente raÃ­z o del elemento padre.
- **`%`**: Relativa al tamaÃ±o del contenedor padre.
- **`vw` y `vh`**: Relativas al ancho y alto del viewport.
- **`vmin` y `vmax`**: Relativas al tamaÃ±o mÃ­nimo o mÃ¡ximo del viewport.
- **`fr`**: Fracciones de un contenedor en un `grid`.
- **`ch`**: TamaÃ±o del carÃ¡cter "0" de la fuente.

---

## Â¿CÃ³mo elegir la unidad adecuada?

### Ejemplos prÃ¡cticos

1. **Texto escalable con `rem`**  
    ```css
    html {
        font-size: 16px; /* Base */
    }

    h1 {
        font-size: 2rem; /* Escala con el tamaÃ±o raÃ­z */
    }

    p {
        font-size: 1rem; /* Igual al tamaÃ±o raÃ­z */
    }
    ```

2. **DiseÃ±os responsivos con `vw` y `vh`**  
    ```css
    .hero {
        height: 100vh; /* Ocupa toda la altura del viewport */
        font-size: 5vw; /* Escala con el ancho del viewport */
    }
    ```

3. **Porcentajes para contenedores flexibles**  
    ```css
    .container {
        width: 80%; /* 80% del ancho del contenedor padre */
        height: 50%; /* 50% del alto del contenedor padre */
    }
    ```

4. **Uso combinado con `clamp()`**  
    ```css
    h1 {
        font-size: clamp(18px, 2vw, 36px); /* MÃ­nimo 18px, mÃ¡ximo 36px */
    }
    ```

5. **Grid Layout con `fr`**  
    ```css
    .grid {
        display: grid;
        grid-template-columns: 1fr 2fr; /* Dos columnas, 1 parte y 2 partes */
    }
    ```

---

## Buenas prÃ¡cticas

1. **Evita redundancias**:  
   Usa `0` sin unidades:
    ```css
    margin: 0; /* Correcto */
    margin: 0px; /* Redundante */
    ```

2. **No definas `line-height` si no es necesario**:  
    ```css
    p {
        font-size: 1rem;
        /* line-height innecesario si no necesitas ajuste especÃ­fico */
    }
    ```

3. **Considera accesibilidad**: Usa `rem` en lugar de `px` para elementos relacionados con texto.

4. **Entiende la relaciÃ³n entre unidades**:  
   Por ejemplo, `em` escala con el padre, mientras que `rem` escala con el tamaÃ±o raÃ­z.

---

## Tabla Resumen

| Unidad  | Relativa a                      | Uso principal                         |
|---------|---------------------------------|---------------------------------------|
| `px`    | Ninguna (absoluta)             | TamaÃ±os fijos                         |
| `rem`   | TamaÃ±o raÃ­z                    | Texto escalable                       |
| `em`    | TamaÃ±o del elemento padre      | Escalado relativo                     |
| `%`     | Contenedor padre               | DiseÃ±os flexibles                     |
| `vw`    | Ancho del viewport             | DiseÃ±os responsivos                   |
| `vh`    | Alto del viewport              | Alturas responsivas                   |
| `fr`    | Contenedor en `grid`           | DistribuciÃ³n en rejillas              |
| `ch`    | Ancho del carÃ¡cter "0"         | Anchos predecibles                    |

---

Con este archivo, puedes recordar cÃ³mo y cuÃ¡ndo usar cada unidad CSS para escribir cÃ³digo eficiente y adaptativo.