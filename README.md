# Detecci-n-de-Smart-Money-vs-Retail-en-Gaps
Detección de Smart Money vs Retail en Gaps

Detección de Smart Money vs Retail en Gaps
Volumen Alto sin Convicción Direccional

Este proyecto implementa una consulta SQL que detecta posibles fases de distribución institucional luego de gaps provocados por noticias, donde el volumen permanece elevado pero el precio deja de avanzar.

La señal busca identificar situaciones donde el mercado parece activo, pero en realidad el dinero informado está saliendo.

🧠 Idea central

Después de una noticia:

el precio abre con un gap

entra volumen masivo

los traders minoristas persiguen el movimiento

Sin embargo, cuando:

el volumen sigue alto

pero el rango diario es estrecho

…suele indicar absorción y distribución, no continuación.

Mucho intercambio, poca convicción.

🎯 Valor de negocio

Identifica trampas de mercado

Útil para:

evitar entradas tardías

detectar techos locales

estrategias contrarian o de mean reversion

Mejora la lectura de flujos post-noticia

🗄️ Estructura de datos esperada
precios_diarios
campo	descripción
ticker_id	Identificador
fecha	Fecha
open	Precio de apertura
close	Precio de cierre previo
high	Máximo diario
low	Mínimo diario
volume	Volumen negociado
tickers
campo	descripción
ticker_id	Identificador
sector	Sector económico
⚙️ Lógica de la consulta

Detecta días con gap de apertura

Calcula:

tamaño del gap

volumen negociado

rango diario de precios

Agrega métricas por sector

Filtra sectores donde:

el volumen promedio es alto

pero el rango de precios es bajo

🔎 Interpretación de resultados

Volumen alto → participación institucional

Rango estrecho → falta de avance real

Conclusión:

absorción de órdenes

distribución silenciosa

alta probabilidad de reversión o lateralización

🚀 Posibles extensiones

Analizar por activo en lugar de sector

Confirmar con delta de volumen

Separar gaps al alza vs a la baja

Incorporar cierre relativo al gap

📝 Notas finales

No es una señal de compra o venta directa

Es una alerta de riesgo oculto

Ideal como filtro post-evento
