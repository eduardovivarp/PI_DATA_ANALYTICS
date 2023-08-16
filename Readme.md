<p align=center><img src=https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png><p>

# <h1 align=center> **PROYECTO INDIVIDUAL Nº2** </h1>

# <h1 align=center>**`Cryptocurrency Markets Data Analytics`**</h1>

<p align="center">
<img src=".\img\imagen1.png"  height=300>
</p>

# <h1 align=center>**`Eduardo Vivar Pomiano`**</h1>
# <h1 align=center>**`Agosto - 2023`**</h1>
<hr>  

## **SERVICIOS FINANCIEROS ABC SAC**

La empresa de Servicios Financieros ABC ha manifestado interés en adentrarse en el  mundo de las criptomonedas. Como una empresa de servicios financieros vanguardista, requiere un informe en base al análisis donde se pueda entender el mercado de las criptos y las recomendaciones para que la empresa pueda incursionar el el mismo. 

## OBJETIVO

El objetivo de este trabajo es realizar una análisis del mercado de las criptomonedas teniendo como principal fuente de informacion la API Coingecko.
Se espera no solo analizar los rendimientos historicos sino tambien ofrecer recomendaciones sobre posibles inversiones o tendencias que se pueden aprovechar.

#### COINGECKO

Esta API a la fecha contiene información de 10031 monedas. Ha sido necesario leer la documentación de esta Api y realizar pruebas para conocer la naturaleza de data que nos ofrece y aplicar esta informacion en nuestro modelado de datos.

La plataforma de coingecko presenta su API en:
[API Cpingecko](https://www.coingecko.com/en/api/documentation)

#### Criptomonedas Seleccionadas
He seleccionado 10 criptomonedas, en dos grupos según ofrece el portal de Coingecko, Top gainers y Top Losers (ordenando por % de ganancia o pérdida, durante las últimas 24 horas), con ambos grupos podemos hacer mas indagaciones sobre un escenario muy optimista y otro que sea totalmente opuesto.
Esta elección además nos da la posibilidad de analizar criptomonedas de grupos heterogéneos a nivel de precios, pero que vienen experimentando crecimiento o pérdida.



## EDA
En el archivo ETL_EDA.jpynb, guardamos los scripts para la carga de informacion invocando a la API, guardamos en dataframes y finalmente almacenamos la informacion en una base de datos MYSQL de forma local.
Las tablas que forman parte del modelo son
+ Coins
+ Coins_selected
+ Price 
+ coin_ROI, esta tabla se creo en mysql, con la informacion de la tabla Price.

## DASHBOARD
En el archivo Dashboard_PI_EDUARDO.pbix se encuentra el dashboard elaborado con Power BI

## REPORTE DE ANALISIS

Son evidentes en base a la investigacion realizada para este proyecto, las caracteristicas de los mercados de las criptomonedas.
Principalmente respecto a su volatilidad. Actualmente hemos podido notar la tendencia a la baja de las principales criptomonedas.

Respecto a la data, es necesario tomar medidas para los casos donde no se tiene informacion completa ya sea del market_cap o del volume. No solamente se puede tratarse de errores de data sino tambien de falta de confiabilidad.


## KPIs
### KPI 1 : Variacion de Precio por Anio - Mes

Evaluando el grafico podemos ver que existen ciertos patrones de ganancias y perdidas que se pueden explorar con mas profundidad
para cada moneda de tal forma que se pueda plantear una estrategia sobre el momento para comprar una criptomoneda, y el momento para vender.

### KPI 2 : Ratio volume / market cap
Se puede conocer la relacion entre el volumen de transacciones de una criptomoneda sobre el tamano de su capitalizacion de mercado o market cap. 

### KPI 3 :  ROI
Este conocido KPI nos permite conocer en un rango de fechas la tasa rentabilidad que un inversor puede lograr al vender una criptomoneda respecto a su valor inicial de compra. 

## Glosario
+ Price / Precio: Es el valor de la criptomoneda en el mercado. Para este documento utilizamos valores expresados en USD.
+ Volume / Volumen: Es el monto total expresado en USD, que representa los montos totales de las transacciones de un periodo determinado de tiempo, ej. las últimas 24 horas.   