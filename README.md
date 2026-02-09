# Evaluaci-n-del-Riesgo-de-Cola
Evaluación del Riesgo de Cola

Evaluación del Riesgo de Cola
Detección de Kurtosis Extremo en Acciones
Descripción General

Este proyecto identifica acciones con riesgo elevado de movimientos extremos de precio, utilizando la kurtosis como métrica central.

Mientras que la volatilidad mide la amplitud promedio de los movimientos, la kurtosis mide qué tan frecuentes y violentos son los eventos extremos.
Una kurtosis significativamente mayor a 3 (valor de una distribución normal) indica colas gruesas (fat tails) y un riesgo no lineal que suele estar subestimado.

Insight Clave

¿Qué acciones presentan una probabilidad anormalmente alta de movimientos extremos?

Un valor de kurtosis elevado revela que:

los retornos no siguen una distribución normal,

los shocks de precio son más frecuentes de lo esperado,

el riesgo real es mayor al percibido por métricas tradicionales.

Valor de Negocio

Identifica activos peligrosos para estrategias de baja volatilidad.

Fundamental para:

gestión de riesgo,

stress testing,

modelos de cola (VaR no paramétrico, CVaR).

Útil para evitar falsas sensaciones de estabilidad.

Detecta activos propensos a:

crashes,

squeezes,

eventos idiosincráticos.

Fuentes de Datos

indicadores_tecnicos

ticker_id

fecha

kurtosis

skewness

Lógica del Análisis

Se analizan los retornos históricos de cada acción.

Se calcula la kurtosis de dichos retornos.

Se filtran los casos donde:

kurtosis > 4.0


indicando colas mucho más pesadas que una distribución normal.

Se ordenan los resultados por severidad del riesgo.

Interpretación de Resultados

Kurtosis ≈ 3
→ Distribución cercana a normal.
→ Riesgo de cola bajo.

Kurtosis entre 4 y 6
→ Riesgo de eventos extremos relevante.
→ Requiere gestión activa.

Kurtosis > 6
→ Riesgo sistémico o idiosincrático severo.
→ No apto para estrategias pasivas sin cobertura.

La skewness complementa el análisis indicando:

si el riesgo extremo está sesgado a pérdidas,

o a ganancias explosivas.

Casos de Uso

Screening de activos de alto riesgo oculto.

Filtrado previo a carteras long-only.

Selección de subyacentes para estrategias de opciones.

Análisis previo a eventos corporativos.

Detección de fragilidad estructural.

Posibles Extensiones

Combinar kurtosis con volatilidad implícita.

Analizar kurtosis por sector o industria.

Medir persistencia del riesgo de cola en el tiempo.

Integrar con skewness para mapas de riesgo asimétrico.

Aplicar umbrales dinámicos según régimen de mercado.

Nota Final

La volatilidad te dice cuánto se mueve el precio.
La kurtosis te dice qué tan violento puede ser cuando se rompe todo.

Este insight no predice eventos,
pero te dice dónde no querés estar cuando ocurren ⚠️📉
