## Conceptos de Sistemas Operativos

### **Tipos de Kernel y sus diferencias**  

Con base a sus características y arquitectura el kernel se podría diferenciar en tres tipos:  

- Monolítico
- Microkernel
- Híbrido

El *kernel Monolítico* centraliza todas las tareas siendo el responsable de gestionar procesos, memorias, comunicación entre procesos, soporte para drivers y hardware, entre otras. No es modular y para modificarlo se requiere compilar el núcleo en sí. Los sistemas más usados como Windows, Linux y Os X utilizan este tipo de núcleo.

El *Microkernel* es un núcleo modularizado lo cual puede permitir que cumpla con las funciones de un kernel mayor, pero su finalidad es precisamente ser un pequeño núcleo que no paralice todo el sistema en caso de fallos. Su finalidad es ofrecer funciones basicos y ser más compactos que otro tipo de núcleos, pueden brindar mayores beneficios en cuando a portabilidad, seguridad y adaptación. Su punto débil puede ser en el manejo de hardware ya que los tiempos de espera de los procesos pueden ser mayores respecto a otros tipos de núcleos.

Los núcleos *híbridos* es la combinación de características entre un kernel monolítico y un microkernel. Pueden incluir código adicional para realizar acciones con más rápidez lo cual lo hacer tener partes cargadas dinámicamente. El kernel mayor debe volverse compacto y modular para poder combinarse con un kernel menor. Los sistemas Linux y OS X incorporan en cierta medida estas características. Otra caractéristica importante de este tipo de núcleo es la posibilidad de escoger qué acciones ejecutar en modo usuario y cuáles en modo superusuario.  

### **User mode y Kernel mode**  
Para una arquitectura x86 existen cuatro modos de operación vá hardware numeros del 0 al 3, los más utilizados en un sistema operativo son el 0 llamado supervisor o modo kernel y el 3 llamado modo Usuario.  

El *modo usuario* ejecuta instrucciones en nombre del usuario.  Consiste en un conjunto de instrucciones que puede ejecutar una aplicación. Ejemplo de estas instrucciones pueden ser add, sub, and, or.

El *modo supervisor* o *kernel* o *monitor* ejecuta instrucciones en nombre del kernel del sistema y son instrucciones privilegiadas. Este modo ofrece acceso a todo el set de instrucciones del procesador. Un fallo de programación en este modo hará que se perdiera el control sobre el sistema e implica tener que hacer un reset.

La diferencia entre ambos modos se marca a través de un bit en el registro de control del procesador y con este bit se diferencias las instrucciones privilegiadas de las normales. Al intentar ejecutar una instrucción privilegiada en modo usuario se produce una excepción.

Para el caso de sistemas Windows el procesador cambia entre los dos modos en función del tipo de código que se ejecuta en el procesador. Las aplicaciones se ejecutan en modod usuario y los componentes principales del sistema en modo kernel.




*Referencias*  
*https://fisop.github.io/apunte/kernel.html*  
*https://keepcoding.io/blog/que-es-el-kernel/*  
*https://learn.microsoft.com/es-es/windows-hardware/drivers/gettingstarted/user-mode-and-kernel-mode*


