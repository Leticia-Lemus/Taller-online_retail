#Online Retail Dataset

### Descripción###

Registros de transacciones de una tienda minorista en línea durante (2010-2011). Contiene facturas, productos, cantidades, precios y países de clientes.

## Campos principales de la base de datos

- InvoiceNo: Número de factura (texto). Ej.: "536365".
- StockCode: Código único del producto (texto). Ej.: "85123A".
- Description: Nombre del producto (texto).
- Quantity: Cantidad vendida (entero). Unidad: "unidades".
- UnitPrice: Precio por unidad (float). Unidad: "libras".
- InvoiceDate: Fecha y hora de la transacción (datetime).
- CustomerID: ID del cliente (float, algunos son nulos).
- Country: País del cliente (texto). Ej.: "United Kingdom".

##Nota: 
- Algunos campos presentan valores nulos o negativos. 
--"CustomerID" presenta clientes no registrados
--"Quantity", "UnitPrice" que indican devoluciones es recomendable filtrarlo.

METADATA POSIBLE: 

 - Intervalo de fechas de las transacciones
-	Número de clientes únicos 
-	Número de productos únicos
-	Ingresos por país
-	 Productos populares por cantidad vendida
-	 Frecuencia de compra del cliente 
-	Valor promedio del pedido

VISUALIZACION

Para representar el análisis de los datos mediante la visualización, se generaron tres gráficos, a fin de representar la distribución de los precios unitarios, la tendencia de ventas por mes y el total de ventas por país.

La gráfica "distribucion_precios"., muestra la distribución de los precios unitarios desde 0 a 8000 dólares.  La desigualdad de en los precios de los productos es deducible, y ayudaría para identificar patrones de venta. Así mismo se puede también observar que es necesario de tratar a los datos para una mejor visualización e interpretación.

La gráfica "tendencia_mensual", representa la tendencia de las ventas mensuales, considerando la suma del campo “TotalAmount” agrupada por mes. En el eje X (Mes) los valores se derivan de las columnas InvoiceDate convertidas a YearMonth. En el eje Y se expresa la suma acumulada de la columna generada TotalAmount (precio unitario por cantidad de producto). Esta figura permite identificar si las ventas aumentan o disminuyen, o bien identificar patrones temporales (temporada navideña).  
 
La gráfica "ventas_por_pais"., se presenta es del tipo  de barras que muestran los volúmenes de compra de 10 países registrados en la base de datos. En el eje Y se muestran los países ordenados de mayor a menor (columna Country). Y el eje X representa el acumulado de las ventas (columna TotalAmpunt). Esta gráfica puede ayudar para identificar cuáles son los países más relevantes para la empresa y hasta alguna dependencia a un mercado. Posible evidencia también de hacer una segunda etapa de revisión de los datos para estandarizar algunos valores.

Conclusión: El análisis exploratorio del dataset Online Retail mostró algunos datos interesantes sobre el comportamiento de las ventas, distribución de precios de los productos y patrones geográficos. Este taller ayudó a generar aprendizajes sobre la manipulación de datos con librerías de Python como Pandas y Seaborn para la visualización. Se puede analizar con más detalle el contenido de la base de datos para extraer más información adicional con diversa posibilidad de aplicación.
