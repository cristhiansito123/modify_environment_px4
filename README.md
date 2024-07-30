# Modificación del entorno de simulación de PX4 Avoidance

![entorno](https://github.com/user-attachments/assets/174f89cf-5114-479b-a18e-3277a3dd28fe)

En este repositorio se explicará el proceso para crear un entorno para editar las variables de ROS, la simulación de PX4 Avoidance de este enlace: https://github.com/PX4/PX4-Avoidance.
También, se explicará como cambiar tanto las variables físicas como visuales tanto del drone como del entorno de simulación, esto nos ayudará a probar algoritmos de navegación autónomas para drones en ROS. Espero les sea de mucha ayuda.

Primero entraremos a la tienda de aplicaciones del sistema operativo. En este caso se encuentra en Ubuntu Software, debido a que es un software licenciado la mejor manera de instalarlo es desde la tienda oficial.

![imagen1](https://github.com/user-attachments/assets/bffad1a2-8ffe-4641-b6ea-807792d57613)

Una vez instalado, lo ponemos en la barra de notificaciones, para que podamos acceder cuando queramos a la aplicación.

![image](https://github.com/user-attachments/assets/d563a47a-feb2-4f15-9458-aea400f2c619)

Desde el apartado de extensiones de visual studio, buscamos ROS en el buscador e instalamos esta dependencia. Esto nos permitirá hacer catkin make y build desde el entorno de visual studio. También nos permitirá ejecutar nodos y editar cualquier archivo que se cree en ROS. Ya sea modelos en gazebo como urdf, proyectos de instalación como cmakelist, etc.

![image](https://github.com/user-attachments/assets/2e09a372-455a-49cb-b58f-d3055ffc26c9)

En este apartado veremos como se ve un proyecto en visual studio, donde podremos acceder a las carpetas del proyecto. Acá podremos ver todos los archivos que componen un proyecto de ROS con su extensión y podremos editarla con autocorrector desde visual studio.
Esto se inicializa desde File y Open Folder, acá buscamos la carpeta src de nuestro proyecto en ROS y obtendremos todas las carpetas con su respectivo formato.

![image](https://github.com/user-attachments/assets/7ff4a09b-3db5-4b49-9061-af131d34566a)

En este archivo podremos modificar las dependencias de nuestro proyecto, como los lenguajes que ejecuta (Python ó C++), compilaciones, versiones que trabaja (Es importante para trasladar los proyectos a otra máquina). Este documento se encuentra principalmente en la raíz de nuestra carpeta de paquetes src, por lo que será fácil ubicarlo.

![image](https://github.com/user-attachments/assets/0aec2351-4ec9-4eee-af43-9de888664951)

Este archivo nos da un enlace directo de todos los paquetes del proyecto, tanto los de lenguaje como los gráficos, entonces acá podremos modificar la ejecución en gazebo ó Rviz. Es crucial e importante en cualquier proyecto y su modificación dependerá de qué queremos ejecutar.

![image](https://github.com/user-attachments/assets/14deff59-308f-4639-b69f-cf0cbbec3b92)

Acá podremos modificar las variables físicas del drone que cambian su desempeño en la simulación, tanto como momento de inercia, masa, tamaño, etc. Esto nos permitirá tener un archivo respaldo a modificar por si en la ejecución física el drone no se mueve de forma estable.

![image](https://github.com/user-attachments/assets/df4fce91-a161-4fe4-afea-6143c8534617)

Una vez tengamos claro los paquetes importantes para la ejecución de un proyecto en ROS, procederemos a modificar los escenarios. Esto se hace desde los archivos ejecutables .launch. Acá podremos observar como cambia el escenario modificando el nombre del ejecutable de la simulación.
![image](https://github.com/user-attachments/assets/7e54e7c9-512e-4026-aa3d-c8be54e34203)

Ahora visualizamos el mundo por defecto que nos ejecuta.

![image](https://github.com/user-attachments/assets/4df7d233-da3a-4481-87cd-67f45bfdf3e0)

Y con el mundo modificado, vemos como nos cambia de escenario.

![image](https://github.com/user-attachments/assets/db886e47-5c69-4a50-b429-037a58e53c98)

Y de esa manera, podremos modificar nuestro escenario desde Visual Studio.
