# Predicción de alquileres de bicicletas
Este repositorio contiene un script de Python llamado ```rentals.py``` que utiliza PySpark para realizar una regresión lineal sobre un conjunto de datos de alquileres de bicicletas. El conjunto de datos se almacena en un archivo CSV llamado ```bike_rentals.csv```.

## Instalación
Para ejecutar el script, deberá tener acceso a un clúster de Spark. Si no tiene un clúster, puede configurar uno en un proveedor de nube como AWS, GCP o Azure. Alternativamente, puede ejecutar Spark en su máquina local en modo independiente.

Una vez que tenga acceso a un clúster, deberá instalar PySpark en su máquina local. Puede seguir las instrucciones en el sitio web de PySpark para instalar PySpark.

## Uso
Para utilizar el script, deberá enviarlo al clúster de Spark utilizando el comando ```spark-submit```. Aquí hay un ejemplo de comando que puede ejecutar en su terminal:

```spark-submit rentals.py```
Este comando enviará el script ```rentals.py``` al clúster de Spark para su ejecución. El script cargará los datos del archivo ```bike_rentals.csv```, los dividirá en un conjunto de entrenamiento y un conjunto de prueba, y entrenará un modelo de regresión lineal en el conjunto de entrenamiento. Luego usará el modelo entrenado para hacer predicciones sobre el conjunto de prueba y mostrará los alquileres de bicicletas predichos junto con los alquileres reales.

Tenga en cuenta que es posible que deba modificar el comando ```spark-submit``` según la configuración específica de su clúster.

## Conjunto de datos
El archivo ```bike_rentals.csv``` contiene datos sobre el alquiler de bicicletas durante un período de 24 horas. Las columnas en el conjunto de datos son:

* hour: la hora del día (0-23)
* temperature: la temperatura en grados Celsius
* visitors: el número de visitantes a la tienda de alquiler de bicicletas durante la hora
* rentals: el número de alquileres de bicicletas durante la hora
