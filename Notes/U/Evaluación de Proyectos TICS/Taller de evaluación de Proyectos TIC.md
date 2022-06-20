# B1

La solución propuesta para el proyecto corresponde a implementar una nueva página/software web, que permita una administración de manera eficiente de productos y que además implemente un sistema de ventas que sea funcional para lo que necesita PRIMA PRESS. Recordemos que este proyecto implica una mejora al servicio que ya se ofrece, por lo que lo anteriormente nombrado corresponde a una mejora sustancial para la empresa.

Por otro lado, es necesario entender que el software que debe ser desarrollado es una extensión que dará continuidad al software que se encuentra hoy en día en marcha. Desde aquí se pueden desprender ciertas restricciones para el proyecto actual tales como:

- Actualmente la página web constituye a un servicio que debe ser mantenido (costos de servidor y mantención). Es por esto que estos precios deben mantenerse luego de la implementación.
- La puesta en marcha del proyecto será una baja para el software antiguo.

Luego, sobre lo que el software debe realizar, se destacan los siguientes puntos:

- Mantener un sistema de stock administrable. En caso de que existan nuevos productos deben poder ser agregados. Cada uno de los productos debe tener estados que permitan manipular la venta de los mismos. Con lo anterior se refiere a que si el administrador desea bloquear, eliminar o cambiar algún valor de un producto, se deberá realizar a través de un panel administrativo.
- Se debe tener un sistema de carrito para la venta de productos, lo que permitirá utilizar un servicio de ventas online que permita al usuario pagar sin mayor problema.
- Un sistema que permita avisarle al cliente cuándo estará la entrega de su producto.

## Descripción de procesos

### Diseño técnico
El diseño técnico del software realizado corresponde a uno que pueda cumplir todos los puntos anteriormente nombrados. Es así como el software debe desarrollarse bajo ciertos puntos:

*Metodología de trabajo*

La metodología de trabajo debe ser cumplido a través de una metodología ágil, que permita ir tratando pequeños puntos de manera semanal, en el periodo de trabajo establecido.

*Administración de servidor* 

La arquitectura empleada corresponde a una arquitectura simple pero escalable. Para esto, en primer lugar se utilizará un deploy en la nube. En el caso, existen diversas opciones de nubes hoy en día:

- AWS
- Azure
- Google Cloud

Todos los servicios mostrados anteriormente ofrecen máquinas con recursos personalizables. Por lo que uno de los parámetros que se utilizaran para elegir a uno de estos elementos corresponde al nivel de seguridad que ofrezcan:

|                                |                        AWS                         |              Azure              |         Google Cloud         |
|:------------------------------:|:--------------------------------------------------:|:-------------------------------:|:----------------------------:|
|         Autenticación          | Identity and Access Management (IAM) Organizations |        Active Directory         |          Cloud IAM           |
|   Protección de información    |                         -                          |  Azure Information Protection   |              -               |
|            Cifrado             |             AWS Key Management Service             |            Key Vault            | Cloud Key Management Service |
|            Firewall            |              Web Application Firewall              |       Application Gateway       |              -               |
|    Evaluación de seguridad     |                     Inspector                      |         Security Center         |              -               |
| Administración de certificados |                Certificate Manager                 |    App Service Certificates     |              -               |
|     Detección de amenazas      |                      GuardDty                      | Azure Advance Threat Protection |        Cloud Security        |
|        Protección DDoS         |                     AWS Shield                     |     DDoS Protection Service     |                              |

Debido a la compración anterior, según los criterios nombrados, se cree que Azure es el sistema que mejor cumple con estándares de seguridad. Por lo que el proyecto debe estar hospedado en Azure.

Por otro lado, el software debe escalar en caso de que la cantidad de personas, debido al flujo de la página web, crezca. Para esto, se utilizará Kubernetes, un software que permite administrar un clúster de contenedores. Es así como se podrán administar réplicas, balanceos de carga y exposición de servicios.

Lo anterior debe ser mantenido por personal que conozca de administración de servidores, que permita también hacer puente directo al desarrollo del software.

*Desarrollo de software*

El desarrollo del software debe ser cumplido por dos personas. En primer lugar debe existir una persona que se dedique al desarrollo del software especializándose en el Front-end. Por otro lado, debe existir una persona que en el desarrollo que sea especializada en el Back-end. Junto al complemento de un desarrollo continuo y ágil, gracias a la combinación de los elementos del proyecto.

