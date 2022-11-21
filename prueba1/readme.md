
# Prueba 1

Diagrama de Red Produzca un diagrama de red (puede utilizar
lucidchart) de una aplicación web en GCP o AWS y escriba una descripción de
texto de 1/2 a 1 página de sus elecciones y arquitectura.

El diseño debe soportar:

• Cargas variables

• Contar con HA (alta disponibilidad)

• Frontend en Js

• Backend con una base de datos relacional y una no relacional

• La aplicación backend consume 2 microservicios externos
El diagrama debe hacer un mejor uso de las soluciones distribuidas


# SOLUCION
![Logo](https://raw.githubusercontent.com/mikeas-it/pruebatecnica/main/prueba1/prueba-aws.png)



#

## Para la resolucion use un ejemplo de una aplicacion web estatica en AWS con alta disponibilidad. Para esta demostracion se utilizo las siguientes herramientas:


[Amazon EC2](https://aws.amazon.com/es/ec2/) : Amazon Elastic Compute Cloud (Amazon EC2) proporciona capacidad de computación escalable en la nube de Amazon Web Services (AWS).

[Amazon Application Load Balancer](https://aws.amazon.com/es/elasticloadbalancing/application-load-balancer/) : Application Load Balancer opera en el nivel de solicitud (capa 7), enrutando el tráfico a los destinos (instancias EC2, contenedores, direcciones IP y funciones de Lambda) según el contenido de la solicitud. Ideal para el equilibrio de carga avanzado del tráfico HTTP y HTTPS, Application Load Balancer proporciona un enrutamiento de solicitudes avanzado destinado a la entrega de arquitecturas de aplicaciones modernas, incluidos los microservicios y las aplicaciones basadas en contenedores.

[Amazon VPC](https://aws.amazon.com/es/vpc/) : Amazon Virtual Private Cloud (Amazon VPC) le brinda control total sobre su entorno de redes virtuales, incluidas la ubicación de los recursos, la conectividad y la seguridad.

[Amazon Auto Scaling](https://aws.amazon.com/es/autoscaling/) : AWS Auto Scaling monitoriza sus aplicaciones y ajusta automáticamente la capacidad para mantener un desempeño predecible y estable al menor costo posible.

[Amazon RDS](https://aws.amazon.com/es/rds/) : Amazon Relational Database Service (Amazon RDS) es una colección de servicios administrados que facilita las tareas de configuración, operación y escalado de una base de datos en la nube.

[Amazon DynamoDB](https://aws.amazon.com/es/dynamodb/) : Amazon DynamoDB es una base de datos NoSQL de clave-valor sin servidor y completamente administrada que está diseñada para ejecutar aplicaciones de alto rendimiento a cualquier escala.

[Amazon Elastic File System](https://aws.amazon.com/es/efs/) : Amazon Elastic File System (Amazon EFS) crece y se reduce automáticamente a medida que se agregan y eliminan archivos sin necesidad de administración o aprovisionamiento.

##
