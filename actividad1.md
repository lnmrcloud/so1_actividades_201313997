# Kernel
## ¿Qué es el Kernel?
Centro de cualquier sistema operativo. Encargado de gestionar las funciones principales del hardware utilizado en el equipo.
## Tipos de Kernel
1.	Kernel monolítico
a.	Solo existe un Kernel responsable de la gestión de recursos para la operación del sistema operativo y sus procesos. Sirve de puente en comunicación entre procesos y funciones con el hardware. 
b.	Gestiona el sistema de archivos, redes, controladores de dispositivos, gestión de memoria, etc. Bajo un mismo “programa”.
c.	Para añadir nuevas funcionalidades, el Kernel debe ser recompilado por completo
d.	Un error o ataque en un proceso puede propagarse a todo el núcleo.
e.	Los sistemas operativos que utilizan este tipo son los de Linux y Windows.
2.	Microkernel
a.	Kernel encargado de funcionalidades especificas con el objetivo de no paralizar todos los demás procesos en el sistema operativo. Aunque puede llegar a cubrir las mismas funciones que un Kernel más grande o monolítico
b.	Tienden a tener una naturaleza modular. Por lo que pueden brindar flexibilidad y facilitad al momento de expandir funcionalidades.
c.	Un error o ataque únicamente puede propagarse en un micronúcleo o Microkernel. 
d.	Al ser muchos, pueden tornar el hardware lento por la alta demanda de recursos en “paralelo”. Se crean colas de solicitudes.
e.	Tiene muy poco uso practico y únicamente se ha utilizado en conjunto con OS X.
3.	Kernel Hibrido
a.	Es la combinación de Kernel monolítico y Microkernel, y por esta misma razón se le llama hibrido. En uno de estos, el Kernel grande(monolítico) se vuelve mas pequeño y centrado en ciertos procesos, mientras que los pequeños (Microkernel) pueden tener funciones dinámicas. 
b.	Poseen las mismas ventajas que un núcleo monolítico y de un Microkernel. Se propone quitar responsabilidad centralizada y distribuirla de forma que el sistema no se torne lento por mucha modulación ni sea totalmente vulnerable en su núcleo principal.
c.	Estos se suelen utilizar en Linux y OS X.
4.	Exonúcleos
a.	Cambian la forma de gestionar el sistema operativo a una estructura vertical, proponiendo el uso de librerías dinámicas que prestan los recursos de memoria y no los maneja como depósitos.
b.	Su principal objetivo es trasladar la carga de memoria a librerías especificas con un alto grado de optimización de recursos.
## Modo usuario vs Modo Kernel
1.	Modo usuario:
a.	Se denota el modo usuario al alcance de los accesos que toda aplicación adquiere al iniciarse en un sistema operativo. 
b.	Programas y procesos que utilicen direcciones de memoria (designadas por estos mismos programas y procesos)
c.	Los accesos en el modo usuario tienen un nivel de privilegio bajo y no se tiene acceso al uso de recursos de forma directa del hardware. (No se escogen o no se puede designar una cantidad especifica)
d.	En modo usuario los programas se ejecutan e inician.
e.	En modo usuario, únicamente se tiene acceso a memoria para usuario en el hardware.
f.	En modo usuario, cada programa tiene una dirección virtual de memoria separada.
g.	Un error en el modo usuario puede ser capturado y controlado, retornando el sistema operativo a la normalidad cerrando el programa o procesos asociados.
h.	El modo usuario puede solicitar utilizar mas recursos de hardware, como utilizar la cámara web, sin embargo, los permisos los gestiona el modo Kernel, y una vez utilizado el recurso regresa al modo usuario.
2.	Modo Kernel:
a.	Se tiene un acceso directo y controlado a los recursos que se necesitan para llevar a cabo programas y procesos, en cualquier momento en el tiempo.
b.	En modo Kernel, los programas tienen acceso ilimitado a los recursos del hardware.
c.	El modo Kernel también se le conoce como: Modo maestro, modo privilegiado o modo sistema.
d.	El modo Kernel tiene acceso a ambas áreas de memoria en el hardware.
e.	En el modo Kernel todos comparten la misma área virtual de memoria.
f.	Un error en modo Kernel puede provocar que el sistema deje de funcionar correctamente y que una recuperación sea muy complicada de ejecutar
## Webgrafía
•	Digital Guide. IONOS. 05/07/2021. https://www.ionos.es/digitalguide/servidores/know-how/que-es-el-kernel/
•	Wizbyte. Tech Area. 04/07/2014. https://wizbyte.wordpress.com/2014/07/04/tipos-de-kernel/
•	Geeksforgeeks. Operating Systems. Kmbh.04/07/2022. https://www.geeksforgeeks.org/difference-between-user-mode-and-kernel-mode/