# Kernel

## ¿Qué es el Kernel?

Centro de cualquier sistema operativo. Encargado de gestionar las funciones principales del hardware utilizado en el equipo.
## Tipos de Kernel

+	Kernel monolítico
    1.	Solo existe un Kernel responsable de la gestión de recursos para la operación del sistema operativo y sus procesos. Sirve de puente en comunicación entre procesos y funciones con el hardware. 
    2.	Gestiona el sistema de archivos, redes, controladores de dispositivos, gestión de memoria, etc. Bajo un mismo “programa”.
    3.	Para añadir nuevas funcionalidades, el Kernel debe ser recompilado por completo
    4.	Un error o ataque en un proceso puede propagarse a todo el núcleo.
    5.	Los sistemas operativos que utilizan este tipo son los de Linux y Windows.
+	Microkernel
    1.	Kernel encargado de funcionalidades especificas con el objetivo de no paralizar todos los demás procesos en el sistema operativo. Aunque puede llegar a cubrir las mismas funciones que un Kernel más grande o monolítico
    2.	Tienden a tener una naturaleza modular. Por lo que pueden brindar flexibilidad y facilitad al momento de expandir funcionalidades.
    3.	Un error o ataque únicamente puede propagarse en un micronúcleo o Microkernel. 
    4.	Al ser muchos, pueden tornar el hardware lento por la alta demanda de recursos en “paralelo”. Se crean colas de solicitudes.
    5.	Tiene muy poco uso practico y únicamente se ha utilizado en conjunto con OS X.
+	Kernel Hibrido
    1.	Es la combinación de Kernel monolítico y Microkernel, y por esta misma razón se le llama hibrido. En uno de estos, el Kernel grande(monolítico) se vuelve mas pequeño y centrado en ciertos procesos, mientras que los pequeños (Microkernel) pueden tener funciones dinámicas. 
    2.	Poseen las mismas ventajas que un núcleo monolítico y de un Microkernel. Se propone quitar responsabilidad centralizada y distribuirla de forma que el sistema no se torne lento por mucha modulación ni sea totalmente vulnerable en su núcleo principal.
    3.	Estos se suelen utilizar en Linux y OS X.
+	Exonúcleos
    1.	Cambian la forma de gestionar el sistema operativo a una estructura vertical, proponiendo el uso de librerías dinámicas que prestan los recursos de memoria y no los maneja como depósitos.
    2.	Su principal objetivo es trasladar la carga de memoria a librerías especificas con un alto grado de optimización de recursos.
## Modo usuario vs Modo Kernel

+	Modo usuario:
    1.	Se denota el modo usuario al alcance de los accesos que toda aplicación adquiere al iniciarse en un sistema operativo. 
    2.	Programas y procesos que utilicen direcciones de memoria (designadas por estos mismos programas y procesos)
    3.	Los accesos en el modo usuario tienen un nivel de privilegio bajo y no se tiene acceso al uso de recursos de forma directa del hardware. (No se escogen o no se puede designar una cantidad especifica)
    4.	En modo usuario los programas se ejecutan e inician.
    5.	En modo usuario, únicamente se tiene acceso a memoria para usuario en el hardware.
    6.	En modo usuario, cada programa tiene una dirección virtual de memoria separada.
    7.	Un error en el modo usuario puede ser capturado y controlado, retornando el sistema operativo a la normalidad cerrando el programa o procesos asociados.
    8.	El modo usuario puede solicitar utilizar mas recursos de hardware, como utilizar la cámara web, sin embargo, los permisos los gestiona el modo Kernel, y una vez utilizado el recurso regresa al modo usuario.
+	Modo Kernel:
    1.	Se tiene un acceso directo y controlado a los recursos que se necesitan para llevar a cabo programas y procesos, en cualquier momento en el tiempo.
    2.	En modo Kernel, los programas tienen acceso ilimitado a los recursos del hardware.
    3.	El modo Kernel también se le conoce como: Modo maestro, modo privilegiado o modo sistema.
    4.	El modo Kernel tiene acceso a ambas áreas de memoria en el hardware.
    5.	En el modo Kernel todos comparten la misma área virtual de memoria.
    6.	Un error en modo Kernel puede provocar que el sistema deje de funcionar correctamente y que una recuperación sea muy complicada de ejecutar
## Webgrafía

+ Digital Guide. IONOS. 05/07/2021. https://www.ionos.es/digitalguide/servidores/know-how/que-es-el-kernel/
+ Wizbyte. Tech Area. 04/07/2014. https://wizbyte.wordpress.com/2014/07/04/tipos-de-kernel/
+ Geeksforgeeks. Operating Systems. Kmbh.04/07/2022. https://www.geeksforgeeks.org/difference-between-user-mode-and-kernel-mode/