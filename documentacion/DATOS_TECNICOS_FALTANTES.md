# Datos técnicos para iniciar simulaciones reales
Estado inicial: no se han recibido ni validado entradas técnicas en este repositorio. Esta lista no afirma que los datos no existan fuera del repositorio.

Para cada dato registrar valor/unidad, archivo o fuente, fecha, revisión, responsable y estado (pendiente/recibido/validado/no aplica). Justificar los no aplicables y cualquier supuesto.

| Bloque | Datos que solicitar o confirmar | Uso |
| --- | --- | --- |
| Identificación | Proyecto, objetivo, buque, variantes, entregables y criterios de aceptación | Definir alcance |
| Casco | CAD de ambos cascos, bulbo, túnel, apéndices; LWL, manga, separación entre centros, superficie mojada y rugosidad | Resistencia e interferencia entre cascos |
| Carga | Desplazamiento/masa, calados proa/popa, trimado, CG y, para movimientos, inercias | Flotación, asiento y movimientos |
| Operación | Velocidades y condición de carga por punto; profundidad, restricciones laterales, agua calma u oleaje | Matriz de simulaciones y dominio |
| Agua | Temperatura, salinidad o propiedades medidas, densidad, viscosidad, presión absoluta y presión de vapor cuando aplique | Reynolds y cavitación |
| Hélices | CAD o secciones completas, diámetro, palas, paso radial, área expandida, skew/rake, núcleo, posición/inclinación, giro y rpm | Empuje, par e interacción casco-hélice |
| Tren propulsor | Curvas de motor, potencia disponible, régimen, relación y eficiencia de reductora, pérdidas del eje y condición de servicio | Comparar demanda con potencia al eje disponible |
| Cavitación | Inmersión, presión ambiente absoluta, propiedades del agua, condiciones de avance/carga y observaciones/ensayos | Definir presión local y validar el modelo |
| Vibraciones | Ubicación/forma de arbotantes, holguras, señales de presión/aceleración con muestreo, rpm, frecuencias/modos, amortiguamiento y condiciones de apoyo estructural | Excitación de palas y respuesta estructural |
| Validación | Ensayos de canal o mar: velocidad, resistencia o potencia/par/rpm, carga, ambiente, incertidumbre y calibración | Cuantificar error del modelo |
| Recursos | Solver y versión/licencia, hardware, presupuesto de cálculo, almacenamiento y permisos de datos | Reproducibilidad y ejecución |

## Condiciones mínimas por etapa
1. **Resistencia en agua calma:** geometría revisada, carga/calados, velocidades, propiedades del agua, profundidad, referencia de validación y decisión sobre asiento/hundimiento fijo o libre.
2. **Hélice aislada:** geometría de pala, rpm, velocidades de avance y propiedades del fluido; referencias de empuje/par.
3. **Autopropulsión:** entradas anteriores, posición de hélices/apéndices y método para equilibrar empuje con resistencia.
4. **Cavitación:** presión absoluta coherente, inmersión, presión de vapor y modelo seleccionado; controles espaciales y temporales específicos.
5. **Vibraciones:** cargas transitorias resueltas, paso de palas y muestreo documentados; modelo estructural o mediciones para evaluar respuesta. El espectro CFD representa excitación, no certifica vibración ni ruido radiado.

## Puerta de revisión
No iniciar una corrida de diseño con pendientes críticos. El responsable debe documentar supuestos aprobados, criterios de convergencia, estudios de sensibilidad y plan de validación. Si aún no hay mediciones, marcar resultados como predicciones no validadas y declarar esa limitación.
