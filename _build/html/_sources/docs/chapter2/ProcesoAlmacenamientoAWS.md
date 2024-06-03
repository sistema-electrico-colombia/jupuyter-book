# Carga de información base de datos AWS.

Luego de realizar el proceso de transformación de la información hemos cargado un dataset unificado de cada una de las variables elegidas del sistema eléctrico Colombiano, y lo hemos dejado en una base de datos aws, con los siguientes datos de conexión.




```python
DB_USER_AWS="postgres"
DB_PASSWORD_AWS="*"
DB_HOST_AWS="analitica-julian-santos.c3mz2sp0n4ch.us-east-1.rds.amazonaws.com"
DB_PORT_AWS="5432"
DB_NAME_AWS="analitica_sistema_electrico"
```

## Descripción proceso de carga

1. Cada uno de los integrantes del grupo creó una cuenta en AWS a traves de AWS Academy

2. Acceder a la consola de Amazon RDS: En Amazon RDS (Relational Database Service) se realiza la creación, configuración, conectividad, operación y características de la base de datos donde almacenamos la información transformada, en la creación es una base de datos con motor de base de datos postgres.

3. Posteriormente, Configuramos opciones adicionales de la base de datos en sus características como el cifrado y las copias de seguridad.

4. Luego nos Conectamos a la base de datos mediante la herramienta DBeaver.

![image1.png](ProcesoAlmacenamientoAWS_files/image1.png)

![image2.png](ProcesoAlmacenamientoAWS_files/image2.png)

![image3.png](ProcesoAlmacenamientoAWS_files/image3.png)
