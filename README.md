# MANZ CFD — Resistencia y propulsión de catamaranes

Base de trabajo de Grupo Manz para organizar geometrías, estudios CFD y evidencia de validación. Estado inicial: sin geometría técnica, mallas ni simulaciones ejecutadas. La plantilla es una especificación de estudio; no es un caso ejecutable de un solver.

## Estructura
| Carpeta | Contenido y relación con proyectos |
| --- | --- |
| geometria/ | Casco doble, separación entre cascos, bulbo, apéndices, hélices y arbotantes; revisiones y sistemas de referencia. |
| mallas/ | Recetas, métricas y refinamientos de superficie libre, estela, palas y zonas de cavitación. |
| casos_cfd/ | Casos de resistencia, hélice aislada, autopropulsión, cavitación y cargas transitorias para vibraciones. |
| resultados/ | Resúmenes de resistencia, potencia, empuje, par, cavitación y espectros de presión/fuerza. |
| scripts/ | Futuras herramientas de preparación, ejecución y posproceso reproducible. |
| documentacion/ | Datos de entrada, decisiones, metodología, validación e informes. |

## Primer caso
1. Completar [los datos técnicos faltantes](documentacion/DATOS_TECNICOS_FALTANTES.md), con fuente y revisión.
2. Copiar `casos_cfd/plantilla/` a `casos_cfd/CAT-001_resistencia_r01/`.
3. Completar `caso.json` y el plan del caso. Los valores `null` están pendientes y nunca equivalen a cero.
4. Elegir solver y versión; preparar sus archivos nativos solo después de revisar entradas, condiciones de contorno y recursos.
5. Verificar geometría, malla, dominio, paso temporal y convergencia; validar con mediciones antes de usar resultados para diseño.

## Convenciones
- SI: m, s, kg, N, N·m, Pa, W; registrar conversión de nudos y rpm.
- Definir origen, ejes, signos, nivel del agua y escala en cada caso; no asumir convenciones de un CAD.
- Cada caso debe identificar revisiones de geometría/malla, commit de scripts, solver, configuración, responsable y fuentes.
- Conservar datos originales sin sobrescribirlos; identificar derivados y supuestos.
- No publicar planos, datos de clientes ni información restringida sin autorización: este repositorio es público.
- Git guarda documentación, configuraciones y resúmenes pequeños. CAD, mallas y campos volumétricos se conservan en almacenamiento externo autorizado con URI, tamaño y SHA-256 en el manifiesto del caso.

## Alcance técnico
Empezar por resistencia en agua calma y balance de fuerzas; continuar con hélice aislada y autopropulsión. Cavitación requiere presión absoluta y presión de vapor coherentes con el agua y la temperatura. Vibraciones requiere cargas transitorias y datos estructurales: CFD por sí solo no determina la respuesta vibratoria del buque.

No se incluyen resultados de rendimiento, parámetros numéricos validados ni una selección definitiva de software.
