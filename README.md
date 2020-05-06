# r8101-dkms-version
How to install:
Step 0: Make sure you have installed the developer tools (build-essential, etc) and kernel headers. If not, then install it first.
Step 1: Install dkms & git in your system
Step 2: Clone this repository
Step 3: Rename the folder to r8101-1.035.02
Step 4: Copy the folder to /usr/src
Step 5: Open a terminal and execute   # dkms add -m r8101 -v 1.035.02
                                      # dkms install -m r8101 -v 1.035.02
Step 6: Blacklist other realtek modules in /etc/modprobe.d/(name of your config file).conf Example: blacklist r8169
Step 7: Reboot.

NOTE: This module includes patches for the following Linux kernel versions: 4.4.x & 5.6.x  Thanks to Sauerland https://build.opensuse.org/project/show/home:Sauerland
DISCLAIMER: I'm not responsible for the misuse of the code or if your system stops working or becomes unstable.

Cómo instalar:
Paso 0: Antes de comenzar checa si tienes instalado las herramientas de compilación para tu distro y las cabeceras del núcleo. De lo contrario instálalo primero.
Paso 1: Instala dkms y git en tu distribución Linux.
Paso 2: Clona este repositorio.
Paso 3: Renombra la carpeta a r8101-1.035.02, esto para que no cause problemas con dkms.
Paso 4: Copia la carpeta a la siguiente ruta /usr/src
Paso 5: Abre una terminal y ejecuta lo siguiente como root # dkms add -m r8101 -v 1.035.02
                                                           # dkms install -m r8101 -v 1.035.02
Paso 6: Agrega a la lista negra otros modulos de realtek que causen conflicto en /etc/modprobe.d/(nombre de tu archivo de               configuración).conf Ejemplo: blacklist r8169
Paso 7: Reinicia.

NOTA: Este módulo incluye algunos parches para que se pueda compilar el módulo en las siguientes versiones del núcleo Linux: 4.4.x y 5.6.x Le doy las gracias a Sauerland por aportar los parches. https://build.opensuse.org/project/show/home:Sauerland
DESCARGO DE RESPONSABILIDAD: No me hago responsable por el mal uso del código, o si su sistema queda inestable o deja de funcionar.
