# Detección de Smart Money vs Retail en Gaps

Volumen Alto sin Convicción Direccional

Este proyecto implementa una consulta SQL que detecta posibles fases de distribución institucional luego de gaps provocados por noticias, donde el volumen permanece elevado pero el precio deja de avanzar.

La señal busca identificar situaciones donde el mercado parece activo, pero en realidad el dinero informado está saliendo.

## 🧠Idea central

Después de una noticia:
- el precio abre con un gap
- entra volumen masivo
- los traders minoristas persiguen el movimiento

Sin embargo, cuando:
- el volumen sigue alto
- pero el rango diario es estrecho

…suele indicar absorción y distribución, no continuación.

Mucho intercambio, poca convicción.

🎯 Valor de negocio

Identifica trampas de mercado

Útil para:

evitar entradas tardías

detectar techos locales

estrategias contrarian o de mean reversion

Mejora la lectura de flujos post-noticia

## 🗄️Estructura de datos esperada

- precios_diarios
- campo	descripción
- ticker_id	Identificador
- fecha	Fecha
- open	Precio de apertura
- close	Precio de cierre previo
- high	Máximo diario
- low	Mínimo diario
- volume	Volumen negociado
- tickers
- campo	descripción
- ticker_id	Identificador
- sector	Sector económico

## ⚙️Lógica de la consulta

Detecta días con gap de apertura

Calcula:
- tamaño del gap
- volumen negociado
- rango diario de precios
- Agrega métricas por sector

Filtra sectores donde:
- el volumen promedio es alto
- pero el rango de precios es bajo

## 🔎Interpretación de resultados

- Volumen alto → participación institucional
- Rango estrecho → falta de avance real

Conclusión:
- absorción de órdenes
- distribución silenciosa
- alta probabilidad de reversión o lateralización

## 🚀Posibles extensiones

- Analizar por activo en lugar de sector
- Confirmar con delta de volumen
- Separar gaps al alza vs a la baja
- Incorporar cierre relativo al gap

## 📝Notas finales

- No es una señal de compra o venta directa
- Es una alerta de riesgo oculto
- Ideal como filtro post-evento

## 👤Autora
Flavia Hepp Proyecto de SQL aplicó un análisis de riesgo basado en eventos.

***
🧠 **El mercado está activo… pero no se mueve. ¿Señal de oportunidad o trampa?**

Imaginá esto:

📈 Hay un gap fuerte en la apertura (noticia relevante)
📊 El volumen explota
😐 Pero el precio… casi no se mueve durante el día

¿Raro, no?

👉 Este patrón suele esconder algo clave:
**distribución de “smart money” hacia inversores minoristas.**

---

🚨 Lo que parece interés… puede ser salida.

En este análisis busqué sectores donde:

* El **volumen promedio es alto** (participación fuerte)
* Pero el **rango diario es bajo** (poca convicción direccional)

💡 Traducción:
Muchas transacciones… pero sin avance real en el precio.

---

⚠️ ¿Qué puede estar pasando?

* Instituciones aprovechando el gap para vender
* Retail entrando tarde, impulsado por la noticia
* Absorción de órdenes sin continuación de tendencia

---

📉 Insight clave:
**No todo volumen confirma una tendencia.**
A veces, confirma exactamente lo contrario.

---

🔍 Este tipo de señales permite detectar:
✔️ Trampas post-noticia
✔️ Falsos breakouts
✔️ Zonas de distribución institucional

---

En mercados financieros, entender *quién está detrás del movimiento* es tan importante como el movimiento en sí.

#Trading #Quant #DataScience #SmartMoney #AnálisisTécnico #Finanzas #MarketMicrostructure
