# Primer cuestionario AWS

1. ¿Qué es informática en la nube?
	- Una entrega bajo demanda de recursos y aplicaciones de TI a través de internet con precios de pago por uso
	- Una ejecución de código sin necesidad de administrar ni aprovisionar servidores
	- Una copia de seguridad de archivos almacenados en dispositivos móviles y de escritorio para evitar perdida de datos
	- Una implementación de aplicaciones conectadas a la infraestructura en las instalaciones

Respuesta: **Una entrega bajo demanda de recursos y aplicaciones de TI a través de internet con precios de pago por uso**. 

Si bien las demás respuestas también se pueden aplicar a la nube, no describen por completo a la misma

2. ¿Cuál es otro nombre para la implementación en las instalaciones?
	- Implementación de nube privada 
	-  Nube de AWS 
	- Implementación hibrida 
	- Implementación basada en la nube

Respuesta: La implementación en las instalaciones también se conoce como **implementación de nube privada**. Este término se refiere a cuando los servicios y la infraestructura se mantienen en las instalaciones privadas de una organización, en lugar de ser alojados por un proveedor de servicios en la nube de terceros.

La **implementación híbrida** es un modelo que combina aspectos de la implementación en las instalaciones y la implementación en la nube. En este modelo, una organización puede mantener algunos recursos en las instalaciones (nube privada) y tener otros recursos alojados por un proveedor de servicios en la nube (nube pública).

La **nube de AWS** es un ejemplo de un proveedor de servicios en la nube, pero no es un término alternativo para la implementación en las instalaciones.

La **implementación basada en la nube** se refiere a cuando los servicios y la infraestructura se alojan completamente en la nube, a menudo a través de un proveedor de servicios en la nube, y no en las instalaciones de una organización.

Por lo tanto, si estás buscando otro nombre para la implementación en las instalaciones, la respuesta más correcta sería “implementación de nube privada”.

3. ¿Cómo le ayuda la escala de la informática en la nube para ahorrar costos?
	- El uso agregado de la nube por parte de un gran número de clientes se traduce en menores precios de pago por uso
	- Puede implementar aplicaciones rápidamente para los clientes y proporcionarles una latencia baja 
	- No es necesario invertir en recursos tecnológicos antes de utilizarlos 
	- El acceso a los servicios bajo demanda ayuda a evitar el exceso o la capacidad limitada

Respuesta: **el uso agregado de la nube por parte de un gran número de clientes se traduce en menores precios de pago por uso** es la respuesta correcta. La escala de la informática en la nube permite a los proveedores de servicios de nube (CSP) amortizar los costos de infraestructura sobre un número mayor de clientes. Esto, a su vez, se traduce en menores precios de pago por uso para los clientes individuales.

Las otras opciones también son beneficios de la escala de la informática en la nube, pero no están directamente relacionadas con el ahorro de costos. La implementación rápida de aplicaciones y la latencia baja son beneficios de rendimiento, mientras que la capacidad bajo demanda ayuda a evitar el exceso o la capacidad limitada.

4. ¿Qué afirmación es válida para la infraestructura global de AWS?
	- Una zona de disponibilidad consta de 2 o más regiones 
	- Una región consta de 2 o más zonas de disponibilidad 
	- Una región consta de una única zona de disponibilidad 
	- Una zona de disponibilidad consta de una única región

Respuesta: **Una región consta de 2 o más zonas de disponibilidad**. Una zona de disponibilidad es un conjunto de centros de datos aislados que se encuentran en la misma región geográfica. Las zonas de disponibilidad están diseñadas para ser independientes entre sí, por lo que si una zona de disponibilidad sufre un evento de interrupción, las cargas de trabajo pueden continuar ejecutándose en las demás zonas de disponibilidad de la región.

5. ¿Cuáles son los 5 pilares del AWS Well-Architected Framework?

Respuesta:   
Los cinco pilares del AWS Well-Architected Framework son:

-   **Excelencia operativa:**  Se refiere a la capacidad de operar y mantener una arquitectura de nube de forma eficiente y eficaz.
-   **Seguridad:**  Se refiere a la protección de la información y los sistemas de la nube de los ataques y la pérdida de datos.
-   **Fiabilidad:**  Se refiere a la capacidad de una arquitectura de nube para cumplir con sus requisitos de disponibilidad y rendimiento.
-   **Eficiencia del rendimiento:**  Se refiere a la optimización del rendimiento de una arquitectura de nube para satisfacer las necesidades de las cargas de trabajo.
-   **Optimización de costos:**  Se refiere a la reducción de los costos de una arquitectura de nube sin comprometer su rendimiento, fiabilidad o seguridad.

Estos pilares se basan en los principios de diseño de AWS, que son:

-   **Diseño centrado en la carga de trabajo:**  Las arquitecturas de nube deben diseñarse teniendo en cuenta las necesidades específicas de las cargas de trabajo que se ejecutarán en ellas.
-   **Diseño de alto nivel:**  Las arquitecturas de nube deben diseñarse a un alto nivel antes de pasar a los detalles.
-   **Diseño modular:**  Las arquitecturas de nube deben diseñarse de forma modular para facilitar la escalabilidad, la flexibilidad y la gestión.
-   **Diseño resiliente:**  Las arquitecturas de nube deben diseñarse para resistir eventos de interrupción.
-   **Diseño seguro:**  Las arquitecturas de nube deben diseñarse para proteger la información y los sistemas de los ataques y la pérdida de datos.

El AWS Well-Architected Framework proporciona un conjunto de mejores prácticas y recomendaciones para cada pilar. Estas prácticas y recomendaciones se basan en la experiencia de AWS y en los comentarios de los clientes.

Al seguir el AWS Well-Architected Framework, las organizaciones pueden crear arquitecturas de nube que sean seguras, fiables, eficientes y rentables.

6. Si su empresa tiene una aplicación que utiliza instancias de Amazon EC2 para ejecutar el sitio web orientado al cliente y las instancias de base de datos de Amazon RDS para almacenar información personal de los clientes. ¿Cómo debe configurar el desarrollador la VPC de acuerdo con las prácticas recomendadas?

Respuesta: **Colocar la instancia EC2 en una subred pública y el RDS en una subred privada.** Esta configuración es una práctica recomendada para mejorar la seguridad de la aplicación.

Las subredes públicas son accesibles desde Internet, mientras que las subredes privadas no lo son. Al colocar la instancia EC2 en una subred pública, se puede acceder a ella desde Internet, lo que es necesario para que los clientes puedan acceder al sitio web. Al colocar el RDS en una subred privada, se restringe el acceso a la base de datos a las instancias EC2 de la misma VPC.

Para implementar esta configuración, el desarrollador debe crear dos subredes en la VPC: una subred pública y una subred privada. La subred pública debe tener una puerta de enlace de Internet para que las instancias EC2 de la subred puedan acceder a Internet. La subred privada no debe tener una puerta de enlace de Internet.

A continuación, el desarrollador debe crear un grupo de seguridad para la subred pública que permita el tráfico HTTP entrante desde Internet. El desarrollador también debe crear un grupo de seguridad para la subred privada que permita el tráfico TCP entrante desde la subred pública.

Finalmente, el desarrollador debe lanzar la instancia EC2 en la subred pública y el RDS en la subred privada.

7. ¿Cuáles son los beneficios de la informática en la nube? (seleccionar 2)
	- Dejar de gastar dinero en la ejecución y el mantenimiento de centro de datos 
	- Mantener la capacidad de infraestructura 
	- Beneficiarse de pequeñas economías de escala 
	- Cambiar gastos variables por iniciales 
	- Aumentar la velocidad y agilidad

Respuestas: **Aumentar la velocidad y agilidad** y **Dejar de gastar dinero en la ejecución y el mantenimiento de centro de datos.**

8. ¿Qué opción es un ejemplo de la responsabilidad del cliente en el modelo de responsabilidad compartida de AWS?
	- Concesión de acceso de usuario a Amazon S3 
	- Desmantelamiento de discos de almacenamiento
	- Parchar una instancia de Amazon RDS
	- Proporcionar seguridad para los centros de datos

Respuesta: La opción correcta es **Concesión de acceso de usuario a Amazon S3**.

9. ¿Que tipo de instancia EC2 utilizaría si necesitara un recurso informático que se utilizaría durante al menos un año completo?
	- Instancia reservada 
	- Bajo demanda 
	- Instancia lambda 
	- Instancia de spot

Respuesta: **Instancia reservada**

10. ¿Qué pilar del Macro de Buena arquitectura de AWS se centra en utilizar los recursos informáticos de forma que cumplan los requisitos del sistema?
	- Eficiencia del rendimiento 
	- Seguridad 
	- Fiabilidad 
	- Excelencia operativa

Respuesta: **Eficiencia del rendimiento**

11. Sí, desea almacenar datos en un servicio de almacenamiento de objetos. ¿Qué servicio de AWS es el mejor para este tipo de almacenamiento?
	- EBS
	- S3
	- Managed Blockchain 
	- EFS

Respuesta: Para almacenar datos en un servicio de almacenamiento de objetos, el servicio más adecuado de AWS sería **S3 (Simple Storage Service)**. AWS S3 es un servicio de 
almacenamiento de objetos que ofrece escalabilidad, disponibilidad de datos, seguridad y rendimiento. Esto significa que puedes usarlo para almacenar y recuperar cualquier 
cantidad de datos, en cualquier momento y desde cualquier lugar. Los otros servicios que mencionaste, como EBS, Managed Blockchain y EFS, tienen diferentes usos y no están 
diseñados específicamente para el almacenamiento de objetos.

12. ¿Que afirmacion describe mejor a Amazon DynamoDB?
	- Servicio que puede utilizar para migrar bases de datos relacionales, bases de datos no relacionales y otros tipos de almacen de datos
	- Un servicio que le permite ejecutar bases de datos relacionales  en la nube de AWS
	- Una base de datos relacional de clase empresarial
	- Un servicio de base de datos de valores clave sin servidor

Respuesta: La afirmación que mejor describe a Amazon DynamoDB es **un servicio de base de datos de valores clave sin servidor.** Amazon DynamoDB es un servicio de base de 
datos NoSQL totalmente administrado que ofrece un rendimiento rápido y predecible con una escalabilidad perfecta. DynamoDB te permite delegar las cargas administrativas de 
operar y escalar una base de datos distribuida, por lo que no tienes que preocuparte por el aprovisionamiento de hardware, la configuración, la replicación, la aplicación 
de parches de software o el escalado de clústeres. Con DynamoDB, puedes crear tablas de base de datos que pueden almacenar y recuperar cualquier cantidad de datos y 
atender cualquier nivel de tráfico de solicitudes