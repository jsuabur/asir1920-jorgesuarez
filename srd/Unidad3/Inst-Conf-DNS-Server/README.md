
# Instalación y Configuración DNS Windows Server

---

## 1. Configuración

Vamos a crear un servidor DNS en una máquina con Windows Server 2016.

![Imagen presentación](./images/2016-dns.jpg)

### 1.1. Zona de búsqueda directa

Empezamos haciendo una nueva `Zona de búsqueda directa` yendo al apartado DNS del Administrador del Servidor y entrando en la carpeta `Zonas de búsqueda directa`.

![](./images/zona-directa.png)

Seguiremos los pasos que nos proponen en la configuración y pondremos un nombre de zona (el que queramos):

* Seleccionamos `Zona Principal` y marcamos la casilla siguiente:
  * `Almacenar la zona en Active Directory`.

![Tipo de Zona](./images/directa-principal.png)

* Marcamos `Para todos los servidores DNS que se ejecutan en controladores de dominio en este dominio:...`.

![Ámbito de replicación de zona de Active Directory](./images/directa-replica-dominio.png)

* Comprobamos que esta todo correcto y finalizamos.

![Finalización del Asistente para nueva zona](./images/directa-resumen.png)

### 1.2. Zona de búsqueda inversa

Tras agregar una nueva `Zona de búsqueda directa`, añadimos una nueva `Zona de búsqueda inversa` con la siguiente configuración:

![](./images/zona-inversa.png)

* Elegimos el tipo de `Zona Principal` y marcamos la opción `Almacenar la zona en Active Directory`.

![Tipo de zona](./images/inversa-principal.png)

* Seleccionamos la opción `Para todos los servidores DNS que se ejecutan en controladores de dominio en este dominio:...`.

![Ámbito de replicación de zona de Active Directory](./images/inversa-replica-dominio.png)

* Elegimos en donde deseamos crear una zona de búsqueda inversa, en nuestro caso marcamos para **direcciones IPv4**

![Zona de búsqueda inversa para IPv4](./images/inversa-ipv4.png)

* Agregamos el *ID de Red* para identificar la zona de búsqueda inversa.

![Nombre de la zona de búsqueda inversa](./images/inversa-red.png)

* Comprobamos que esta todo correcto y finalizamos.

![Finalización del Asistente para nueva zona](./images/inversa-resumen.png)

### 1.3. Configurar reenviadores de DNS



![](./images/.png)

## 2. Configurar el servidor para Servidor DNS Caché



![](./images/.png)

## 3. Configurar servidor como DNS Maestro



![](./images/.png)

## 4. Comprobación en el Servidor



![](./images/.png)

## 5. Comprobación en el cliente



![](./images/.png)
