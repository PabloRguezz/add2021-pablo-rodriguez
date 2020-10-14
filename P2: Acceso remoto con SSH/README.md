# **P2: Acceso remoto con SSH**
## **1. Preparativos**
Para comenzar con la práctica necesitaremos lo siguiente:
* Un servidor SSH - GNU/Linux OpenSUSE (Sin entorno gráfico) - 192.168.0.31 - server05g
* Un cliente SSH - GNU/Linux OpenSUSE - 192.168.0.32 - client05g
* Un servidor SSH 	Windows Server 	192.168.0.11 	server05s
* Un cliente SSH 	Windows 	192.168.0.12 	cliente05w

Configurar el servidor GNU/Linux con siguientes valores:
* SO GNU/Linux: OpenSUSE - Sin entorno gráfico.
* Nombre de equipo: server05g
* Poner clave compleja al usuario root.
* Añadir en **"/etc/hosts"** los equipos client05g y client05w.

Crear los siguientes usuarios en server05g:

  * rodriguez1
  * rodriguez2
  * rodriguez3
  * rodriguez4

Instalaremos el software cliente SSH en Windows. Para este ejemplo usaremos PuTTY.
Configurarwmos el cliente2 Windows con los siguientes valores:
  * SO Windows
  * Nombre de equipo: clientXXw
  * Configuración de las MV's
  * Añadir en **"C:\Windows\System32\drivers\etc\hosts"** los equipos server05g y client05g.

 Para realizar esto deberemos ir a la carpeta **"C:\Windows\System32\drivers\etc"**, cuando estemos aquí ejecutamos el siguiente comando:


    "notepad hosts"

  Al realizar esto se nos abrirá el bloc de notas en donde podemos poner las ips.

## 2. Instalación del servicio SSH
Instalaremos el servicio SSH en la máquina serverXXg. Por comandos o entorno gráfico.

  * Desde la herramienta yast -> Instalar Software
  * Desde terminal **"zypper search openssh"** muestra los paquetes instalados o no con nombre openssh*.
  * Desde terminal **"zypper install openssh"**, instala el paquete OpenSSH.Desde el propio servidor, verificar que el servicio está en ejecución.

      systemctl status sshd, esta es la forma habitual de comprobar los servicios.
      ps -ef|grep sshd, esta es otra forma de comprobarlo mirando los procesos del sistema.
