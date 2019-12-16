
# Apache Linux

---

Práctica basada en la instalación y configuración de `Apache`, `PHP`, `MySQL`, `phpMyAdmin` y `SSL` en una MV Linux.

## 1. Configuración Apache y PHP

### 1.1. Apache

Primeramente instalaremos apache2 en nuestra máquina virtual.

> En mi caso, ya lo tenía instalado.

![](./images/inst-apache.png)

Para comprobar que se ha instalado correctamente, entramos en nuestro navegador y vamos a `localhost` y nos tiene que salir la siguiente página:

![](./images/local-apache.png)

En el fichero `/etc/hosts` añadiremos la IP de nuestro equipo con el nombre `miempresa.com` y `www.miempresa.com`.

![](./images/etc-empresa.png)

---

### 1.2. PHP

Ahora instalaremos `PHP`.

![](./images/inst-php.png)

Para que estén confgurados correctamente tanto Apache como PHP necesitaremos instalar la librería `libapache2-mod-php`.

![](./images/inst-lib.png)

Tras instalarla, creamos el fichero `/var/www/html/index.php`

![](./images/phpinfo.png)

Comprobaremos que esta bien configurado entrando a `www.miempresa.com` en un navegador. Tiene que salirnos un recuadro con la versión de PHP instalada.

![](./images/nav-php.png)

---

## 2. Virtual Hosts

Para empezar, haremos el virtualhost `www.empleados.miempresa.com`, para ello, crearemos el fichero `/etc/apache2/sites-available/empleados.conf`.

![](./images/empleados-conf.png)

Tras esto crearemos un enlace simbólico en `/etc/apache2/sites-enabled` para activar el virtualhost.

![](./images/enlace-sim.png)

Para finalizar la configuración, añadiremos el virtualhost al fichero `/etc/hosts` y después crearemos un index y carpeta en `/var/www` para configurar la página web de `www.empleados.miempresa.com`


**/etc/hosts**
![](./images/emp-hosts.png)

**/var/www**
![](./images/emp-index.png)

Comprobamos en nuestro navegador que funciona correctamente.

![](./images/emp-web.png)

---

## 4. SSL

Cuando se instala Apache, conjuntamente se instala el `SSL`. Generaremos un certificado autofirmado ejecutando los siguientes comandos.

![](./images/rsa-key.png)

![](./images/rsa-csr.png)

![](./images/rsa-crt.png)

---

## 5. Virtual Host (Pagos)

Añadimos el fichero `pagos.conf` en los sitios activos de nuestro servicio apache.

![](./images/pagos-conf.png)

![](./images/enlace-pagos.png)

Creamos la carpeta y fichero `/var/www/pagos/index.html`.

![](./images/pagos-index.png)

Añadimos el virtualhost al fichero `/etc/hosts`

![](./images/pagos-hosts.png)

---
