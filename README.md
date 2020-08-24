# AWS aurora

Este ejercicio es para conocer las características generales del servicio de [Aurora AWS](https://aws.amazon.com/es/rds/aurora/).

El objetivo es aprender:
 - Hacer una base de datos Aurora
 - Conectarse con un cliente
 - Hacer respaldos
 - Restaurar nuestra BD


## Instrucciones

Hacer **Fork** de este repositorio en tu cuenta de GitHub.

Los servicios que ocuparemos en este taller son:
 - Region AWS Virginia (us-east-1)
 - S3
 - Aurora
 - Cloud9
 
### Configuración general del ambiente de trabajo
   
   -  Seleccionar Virginia (us-east-1)
   
   -  Entrar y clonar el repositorio en un ambiente de cloud9
    
###  Configurar nuesta base de datos

   - 1  En la pantalla Amazon RDS, ubicado al centro, seleccione **Create databse**.
    ![](https://d1.awsstatic.com/screenshots/10-min-tut-aurora-autoscaling/autoscaling-1.3.1.4f1479d5b9cde064538c4f4aaf479ac893135776.png)
    
 - 2 En el motor de base de datos, seleccione **Amazon Aurora** .
    ![](https://d1.awsstatic.com/screenshots/10-min-tut-aurora-autoscaling/autoscaling-1.4.2f8f85673625fc52b18604f39998742479ea3ace.png)

   - 3 En Edición, seleccione **Amazon Aurora con compatibilidad con MySQL**.
    ![](https://d1.awsstatic.com/screenshots/10-min-tut-aurora-autoscaling/autoscaling-1.4.2f8f85673625fc52b18604f39998742479ea3ace.png)
    
    
  -  4 En Versión, seleccione su versión preferida de Aurora.
    ![](https://d1.awsstatic.com/screenshots/10-min-tut-aurora-autoscaling/autoscaling-1.6.0abf12afd092721466c71329f05ea05ed0204e6c.png)
    
    
  -  5 Elija un identificador para su clúster de base de datos de Aurora, por ejemplo **database-1** .
    ![](https://d1.awsstatic.com/screenshots/10-min-tut-aurora-autoscaling/autoscaling-1.10.5a485df49d06c7aba9d2d442021ac6641c1c1646.png)
    
    
   -  7 Seleccione la VPC donde desea crear la base de datos. 
   **Tenga en cuenta que una vez creada, la base de datos no se puede migrar a una VPC diferente**.
    ![](https://d1.awsstatic.com/screenshots/10-min-tut-aurora-autoscaling/autoscaling-1.13.608f43a3c074e4acf3bd53bac32065fca4cf92db.png)
   
  -  8 Seleccione la VPC donde desea crear la base de datos. 
    ![](https://d1.awsstatic.com/Getting%20Started/Boosting%20Database%20Performance/image065.6fb24cf5a5d42556e7b59e493264453976206c39.png)
    





### Generarlo con CloudFormation

1. Run instructions

    ```bash
	aws cloudformation create-stack --stack-name aurora --template-body file://Aurora.yml --parameters file://stack-01.json
    ```

2. Delete all 

    ```bash
	aws cloudformation delete-stack --stack-name aurora 

    ```


