---
layout: single
title: "Cómo optimizar el rendimiento de las plantas PV antiguas del régimen especial"
categories: blog
tags:
  - Opinion
  - Renewables
  - Solar
  - Sustainability
  - Business
  - Infrastructure
  - Sales
  - SaaS
  - Spanish
classes: wide theme-dark
date: 2020-07-14 10:46:57 +0100
excerpt: Las energías renovables en España en los últimos 15 años tienen para una historia digna de una serie de ficción. En un resumen muy simple, cuando se empezó a incentivar la Fotovoltaica, su retribución era tan alta que creo una burbuja de instalación de plantas, cuya explosión ha tenido consecuencias políticas y legales por muchos años.
header:
  overlay_image: /assets/images/solarPV.jpeg
  teaser: /assets/images/solarPV.jpeg
---

# Cómo optimizar el rendimiento de las plantas PV antiguas del régimen especial

![Optimiza el rendimiento monitoreando los contadores](/assets/images/solarPV.jpeg "Optimiza el rendimiento monitoreando los contadores")

Las energías renovables en España en los últimos 15 años tienen para una historia digna de una serie de ficción. En un resumen muy simple, cuando se empezó a incentivar la Fotovoltaica, su retribución era tan alta que creo una burbuja de instalación de plantas, cuya explosión ha tenido consecuencias políticas y legales por muchos años.

Tras varios miles de páginas en normas y regulaciones, finalmente la retribución de las plantas se basa en lo que puedan conseguir vendiendo en el mercado (a pool) más una retribución específica, marcada por el Ministerio. Se determina en base a unas tablas que garantizan una rentabilidad razonable en torno al 7% o a base de subastas en las plantas nuevas.

Por tanto, es importante optimizar y conseguir un balance adecuado entre la cantidad invertida en O&M y el retorno de la inversión, en función de cómo es su retribución.

Para las plantas nuevas, que van a mercado o firman PPAs, los precios son muy competitivos, por lo que cada kWh generado es vital para asegurar la rentabilidad. Ello requiere una operación y mantenimiento exhaustivos, para producir el mayor número de horas posible. Para ellas, el uso de herramientas de monitoreo modernas, como Qantum de QOSEnergy, ayuda a que cada rayo de sol se aproveche de la mejor manera. Necesitan monitorear casi todas las variables que proporcionan los inversores, dataloggers, sondas, etc. Afortunadamente, los nuevos equipos tienen forma de exportar los datos con protocolos IoT, que permiten su fácil integración en herramientas SaaS de gestión de portfolios como Qantum.

## Bajo incentivo a la excelencia en la operación en plantas antiguas

Sin embargo, las plantas antiguas tienen retos diferentes. En este caso, tienen menos incentivo a incrementar la producción, pero más incentivo a optimizar los costes de O&M. Por ello, no suelen necesitar analíticas avanzadas, pero si vigilar ciertos KPI de forma económica que garanticen niveles de rendimiento suficientes.

De forma sencilla, su retribución deriva de unas tablas que la comparan con la de una instalación tipo eficiente y bien gestionada, y está basada en tres componentes:

```
Retribución total = Retribución a la Inversión (80-90%) + Retribución a la Operación (3-10%) + Venta a mercado (7-13%)


```

- Retribución a la Inversión: Supone el 80-90% del total. Es un pago en función de la capacidad instalada (EUR/MW), siempre y cuando se supere un umbral de horas equivalentes de producción. El umbral es bastante pequeño, entre 500 a 1000 horas al año, y la retribución se pondera por unas horas mínimas equivalente entre 900 y 1200h. Es decir, consiguiendo apenas que la planta este funcionando y vierta a red, casi se garantiza la mayor parte de los ingresos.
- Retribución a la Operación: Supone el 3-10% del total. Es un pago en función de las horas equivalentes producidas para compensar los gastos operativos, hasta un límite de horas en torno a las 1600-1800h aprox.
- Venta a mercado: Supone entre un 7-13% de la retribución total dependiendo del precio del pool y de la energía vertida.

Por tanto, por encima de las horas equivalentes mínimas no hay mucho incentivo a operar más horas. Incluso, superadas las horas máximas, sólo se retribuye a precio de mercado.

En lo últimos años, el precio del pool ha estado en torno a los 50EUR/MWh. Es decir, por ejemplo, producir una hora equivalente más por encima del máximo en una instalación solar de 1MW, nos retornaría tan sólo unos 50euros.

(Y este año incluso menos, ya que por el COVID los precios de 2020 están alrededor de 29EUR/MWh)

## Monitorización orientada a superar mínimos

Por tanto, bajo esta estructura, la mejor estrategia es un monitoreo sencillo y económico que permita detectar problemas importantes y actuar en unos días. No es imprescindible un monitoreo detallado o una respuesta rápida, con el objetivo de maximizar la producción, porque los costes de ello, probablemente superen los ingresos, cuando ya hemos superado las horas equivalente mínimas. Por supuesto, cuanto más se produzca, mayor será el ingreso total, pero los últimos euros ganados serán comparativamente muy bajos.

El sistema de monitoreo tiene que estar orientado a garantizar que la planta funciona más que el umbral y más que el mínimo de horas equivalentes. Como esos limites son bajos, esto prácticamente se consigue si la planta vierte a red de forma diaria, con un mantenimiento justo. Pero en todo caso, es clave alcanzar este mínimo, y por ello, un monitoreo básico sí que es necesario.

La solución habitual y suficiente es monitorear los contadores de vertido a red. Dado que han de estar conectados a internet de todas formas para que las distribuidoras puedan leerlos, es una manera sencilla de tener acceso a los datos. Y nos permite saber si la planta funciona y cuánta energía ha vertido.

![Optimizacion planta solar con datos](https://media.licdn.com/dms/image/C4D12AQF0CK1mo5-u1A/article-inline_image-shrink_1000_1488/0/1598530087789?e=1720656000&v=beta&t=Ygz-kuneHDFb-HNUgltygtz14se-LQ2PYGHhbhpCJvg)

Si el SCADA o los inversores también están conectados a red, y los datos son accesibles, también se pueden monitorear, pero en estas instalaciones antiguas, esto muchas veces implica cierta inversión en dataloggers o upgrades, que no se justifican con los ingresos.

La dificultad tradicional con los contadores es que la comunicación no es muy estable y sistemas poco avanzados devuelven archivos con gaps que luego hay que rellenar manualmente. Además, la salida son archivos CSV que hay que trabajar tediosamente con Excel.

En Qantum podemos incorporar sin gaps tanto datos de contadores IP como GSM. Los primeros con una frecuencia de 15minutos y los segundos usualmente varias veces al día. Además, incorporamos datos de irradiación satelital a partir de las coordenadas GPS, lo que nos permite calcular Performance Ratios (PR) de forma sencilla. La configuración de este tipo plantas sólo toma un par de días y se puede incorporar el histórico de datos. Al ser una herramienta Cloud, no es necesario instalar nada y los dashboard son accesibles desde cualquier navegador, por distintos usuarios.

![Optimizacion planta solar](https://media.licdn.com/dms/image/C4D12AQGJYIH4JN-eaw/article-inline_image-shrink_1000_1488/0/1598530298444?e=1720656000&v=beta&t=Qebp7mmF_528f11hMot6ncLtzw01gh3sZra1hmFi1YI)

Con Qantum, se pueden configurar alarmas y gestionar los tickets de mantenimiento de forma sencilla, al nivel del O&M que requieren estas plantas. Además, se puede automatizar la generación de informes resumen, que permite un ahorro de tiempo esencial para liberar al equipo de estas operaciones tediosas, que no aportan valor y consumen recursos.

De esta forma, con una sola herramienta, se puede gestionar todo el portfolio renovable, ya sean plantas nuevas con necesidad de mucha información o plantas antiguas donde casi sólo hay que garantizar su funcionamiento.
