
# FTP - Prácticas Windows y Linux

---

## 1. FTP - Windows

---

## 2. FTP - Linux

### 2.1. Instalación

Comenzaremos instalando el **servicio SSH** en el `servidor Linux`.

![](./images/linux-1-install-ssh.png)

### 2.2. Usuarios FTP

Tras instalarse correctamente, creamos *dos usuarios* en el servidor, con diferentes privilegios y niveles de acceso al `filesystem`, en mi caso son:
* usu-ftp1
* usu-ftp2

**usu-ftp1**

![](./images/linux-2-usu-ftp1.png)

**usu-ftp2**

![](./images/linux-3-usu-ftp2.png)

![](./images/linux-4-usu-ftp2-root.png)
![](./images/linux-5-usu-ftp2-root.png)

Ahora comprobamos que se han creado correctamente las cuentas de usuario con los distintos privilegios.

![](./images/linux-6-usu-ftp1-comp.png)

![](./images/linux-7-usu-ftp2-comp.png)

### 2.3. Acceso SSH

Comenzaremos conectándonos desde el cliente con los usuarios anteriores.

![](./images/linux-8-usu-ftp1-ssh.png)

![](./images/linux-9-usu-ftp2-ssh.png)

Ejecutaremos una aplicación gráfica del **servidor** de forma remota desde el **cliente** mediante `ssh`.

> En mi caso ejecutaré *geany*, si lo quisieran utilizar también este programa habría que instalarlo ya que no viene predeterminado en el sistema.
> Para instalarlo por comandos, utilizaremos **sudo apt install geany**.

Comando para ejecutar la aplicación gráfica remota:
* ssh -X -p 22 usu-ftp1@172.19.15.21 geany

![](./images/linux-10-usu-ftp1-geany.png)

## 2.4. SFTP

Ahora accederemos al servidor mediante `SFTP` *(SSh File Transfer Protocol)* con los dos usuarios creados.
Buscaremos los ficheros creados en cada cuenta de usuario para descargarlos en el cliente.

Usuario   | Fichero                             |
:-------: | :---------------------------------: |
usu-ftp1  | /home/usu-ftp1/file-download-1.txt  |
usu-ftp2  | /home/usu-ftp2/file-download-2.txt  |

**usu-ftp1**

![](./images/linux-12-usu-ftp1-download.png)

**usu-ftp2**

![](./images/linux-13-usu-ftp2-download.png)