# ProgIIIG101-Act05-DylanCardenasPerez
# Actividad 05 – Estructuras y Listas en Prolog

**Programación III – G101 | Universidad Tecnológica de Pereira**

## Descripción

Modificación de dos programas Prolog para reemplazar hechos individuales por **listas y estructuras**, usando `member/2` para navegar las listas. Las consultas originales siguen funcionando sin cambios.

## Archivos

| Archivo | Descripción |
|---|---|
| `simpson_listas.pl` | Familia Simpson con `padre_de/2`, `madre_de/2` como listas |
| `canada_listas.pl` | Ciudades de Canadá con `conexiones/2` usando estructuras `destino/2` |

## Cambio principal

**Antes:**
```prolog
padre(homero, bart).
padre(homero, lisa).
padre(homero, maggie).
```

**Después:**
```prolog
padre_de(homero, [bart, lisa, maggie]).
```

Las reglas usan `member/2` para recorrer las listas:
```prolog
es_padre(Padre, Hijo) :-
    padre_de(Padre, Hijos),
    member(Hijo, Hijos).
```

## Consultas de ejemplo

```prolog
?- es_padre(homero, Hijo).
?- abuelo(Abuelo, bart).
?- rutaConCosto(vancouver, winnipeg, Costo).
```

## Autor

Dylan Cárdenas Pérez
