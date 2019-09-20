
# Instalaciones y configuraciones previas

---

> ¡OJO!: Poner la red en adaptador puente en todas las máquinas.

## 1. Ubuntu 16 Cliente

### 1.1. Instalación

Empezamos instalando Ubuntu 16.

![Primeros pasos](./images/inicio.png)

Ponemos la configuración predeterminada y seguimos con la instalación.

![Instalando](./images/instalacion.png)

### 1.2. IP estática

Ahora que está instalada correctamente, configuramos la IP estática y comprobamos.

![IP estática](./images/ip-ubuntu-cliente.png)

![Comprobación Ubuntu16](./images/comp-u16.png)

---

## 2. Ubuntu 16 Servidor

### 2.1. Instalación

Clonaremos Ubuntu 16 y después cambiaremos la MAC para que no haya problemas de compatibilidad.

![Clonación](./images/clonacion.png)

### 2.2. IP estática

Ahora configuramos la IP estática.

![IP estatica Ubuntu Server](./images/ip-ubuntu-server.png)

![Comprobación Ubuntu Server](./images/comp-u16-server.png)

---

## 3. Windows 7

Instalamos Windows7 con la configuración predeterminada y ponemos la IP estática.

![IP Windows](./images/ip-windows7.png)

---

## 4. Windows 2016 Server

### 4.1. Instalación

Ahora instalaremos Windows Server 2016 Standard.

![Instalación Windows Server 2016](./images/inst-ws2016.png)

### 4.2. IP estática

Configuramos la IP estática del server y comprobamos si está todo hecho correctamente.

![IP estática Windows Server 2016](./images/ip-windows2016.png)

### 4.3. Active Directory

Utilizaremos Active Directory para la creación de grupos, usuarios del dominio y unidades organizativas.

![Active Directory](./images/active-directory.png)

**Creación del Dominio**
Entramos en `Agregar Roles y/o características` y agregamos `Servicios de Active Directory`.
Una vez completada la instalación, marcamos `Promover Windows 2016 a Controlador de Dominio`.

* Para empezar crearemos el dominio, así que utilizaremos la opción `Agregar un nuevo bosque` con el nombre del dominio.

![Nuevo bosque](./images/nuevo-bosque.png)

* El siguiente paso, es seleccionar el nivel funcional del bosque y una contraseña de *modo de restauración de servicios de directorio (DSRM)*

![Nive funcional del bosque](./images/nivel-funcional.png)

**Grupos del dominio**



![](./images/.png)

**Usuarios del dominio**



![](./images/.png)

**Unidades Organizativas**



![](./images/.png)

**Enlazar Windows7 (Cliente) al dominio**



![](./images/.png)
