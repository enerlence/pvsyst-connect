# Ejemplos de peticiones

Una vez que el conector está activado, habla con el asistente como lo
harías con un compañero que tiene PVsyst abierto. Cambia los nombres de los
proyectos por los tuyos.

## Explorar

> Lista mis proyectos de PVsyst y dime cuáles ya tienen resultados de
> simulación.

> Resume el sistema del proyecto «Nave», variante VC0: módulos, inversores,
> potencia pico, orientación y las principales pérdidas.

> Audita los parámetros de la variante VC1 de «Nave» y señala cualquier
> cosa fuera de lo normal (soiling, mismatch, factor térmico, albedo).

## Simular

> ¿Cuántas ejecuciones de licencia de PVsyst me quedan?

> Lanza la simulación de la variante VC0 de «Nave» y enséñame la
> producción mensual y el diagrama de pérdidas.

> Compara inclinaciones de 15°, 20°, 25° y 30° para «Nave» en un único
> batch y dime cuál da el mayor rendimiento específico.

> Quiero ver este mismo sistema en Ginebra y en Madrid. Crea ambos sites y
> simula con meteorología sintética.

## Informe

> Prepara un informe de resultados de «Nave» VC0 con gráficos y dame el
> enlace de descarga del PDF.

> Dame los resultados horarios de la última simulación en CSV.

## PV*SOL (solo lectura)

> Lista mis proyectos de PV*SOL y enséñame el autoconsumo, el vertido a
> red y la cobertura solar de «Casa García».

> Enséñame la cascada de pérdidas de mi proyecto de PV*SOL «Casa García»,
> desde la irradiación horizontal hasta la energía entregada.

## Es bueno saberlo

- Un batch de simulaciones cuesta una sola ejecución de licencia, sea cual
  sea el número de casos que contenga; el asistente lo usa para hacer
  comparativas.
- Los workflows como «optimizar la orientación», «comparar dos variantes» o
  «evaluar varias ubicaciones» ya vienen integrados: pregunta *«¿Qué
  workflows tienes para PVsyst?»*.
- Si una petición queda bloqueada por tus permisos, el asistente te lo
  dirá. Solo tú puedes cambiarlos, en Suntropy Connect.
