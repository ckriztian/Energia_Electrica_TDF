### *Características del Dataset* 

Nombre original del DataSet: 15_3_01_Energia_electrica_consumida_por_tipo_usuario-5.xlsx

Cantidad de instancias: 182

Cantidad de columnas/variables: 8

El dataset está compuesto por las siguientes variables: 

- **Periodo**: Subdivido en año y mes, durante el cual se mide el consumo de energía. 
- **Total**: Corresponde a la cantidad total de energía eléctrica facturada en la Provincia de Tierra del Fuego. 
- *Tipo de usuario*: Categorización de los usuarios según el nivel de demanda 
y tipo de consumo, incluyendo: 
- **Grandes Demandas**: Corresponde a la cantidad de energía eléctrica facturada por la población usuaria de grandes demandas en la Provincia de Tierra del Fuego, categoría que aplica a clientes cuya demanda máxima de potencia contratada sea igual o mayor a  50 kW.
- **Medianas Demandas**: Corresponde a la cantidad de energía eléctrica facturada por la población usuaria de medianas demandas en la Provincia de Tierra del Fuego, categoría que aplica a clientes cuya demanda máxima de potencia contratada sea mayor a 10 y menor a 50 kW.
- **Uso Residencial**: Corresponde a la cantidad de energía eléctrica facturada por la población usuaria de uso residencial en la Provincia de Tierra del Fuego, categoría que aplica a usuarios con uso final declarado residencial y con demanda máxima de potencia no superior a los 10 kW.
- **Uso General**: Corresponde a la cantidad de energía eléctrica facturada por la población usuaria de alumbrado público en la Provincia de Tierra del Fuego,categoría que aplica a clientes con uso final no residencial (usos comerciales, industriales, servicios, oficiales, etc.) y cuya demanda máxima de potencia no supere los 10 kW.
- **Alumbrado Público**: Son aquellos usuarios que utilizan la energía eléctrica con la finalidad de iluminar espacios de dominio público. El alumbrado público de las Ciudades de Ushuaia y Tolhuin no se mide, se calcula en función de la cantidad de lámparas instaladas y horas de funcionamiento.

*Tipo de datos*:

| Variable | Tipo de Dato | 
|----------|----------|
| Año    | int64   | 
| Meses    | float64   | 
| Total    | float64   | 
| Grandes Demandas    | float64   | 
| Medianas Demandas    | float64   | 
| Uso Residencial    | float64   | 
| Uso General    | float64   | 
| Alumbrado Público    | float64   | 

*Fuente:* Dirección Provincial de Energía Ushuaia y Cooperativa Eléctrica y Otros Servicios Públicos Ltda.
(https://ipiec.tierradelfuego.gob.ar/)



### *Archivos de Dataset y Documentos*

El dataset y los documentos relacionados están incluidos en el repositorio GIT en las siguientes ubicaciones:

~~~
- data/raw: Contiene los datos originales sin procesar.
- data/interim: Contiene los datos intermedios que han sido transformados.
- data/processed: Contiene los datos finales listos para el modelado.
- references: Puede contener manuales, diccionarios de datos y cualquier otro material explicativo relevante.
~~~

Se recomienda revisar estos archivos y documentos para obtener una comprensión completa de los datos y su contexto antes de proceder con el análisis y el desarrollo de modelos de aprendizaje automático.