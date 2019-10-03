
# Instalación y Configuración DHCP Windows

---

## Introducción

Utilizaremos dos máquinas virtuales:
* MV1: Windows2016 Server
* MV2: Windows

Antes que nada, pondremos nuestras MV's en `Red Interna`.

---

## 1. Instalación DHCP Windows 2016 Server

Para su instalacion, vamos a `Agregar roles y características` que se encuentra en el `Administrador del servidor` en el apartado `Administrar`. Tras esto, seleccionamos `Servidor DHCP` y lo instalamos.

![Seleccionar Servidor DHCP](./images/servidor-dhcp.png)

![Instalación DHCP](./images/instalar-dhcp.png)

---

## 2. Configuración del servicio DHCP

Para configurar el servicio DHCP, tendremos que acceder a la sección `DHCP` de `Herramientas` del Administrador del Servidor.

![DHCP](./images/dhcp.png)

Seguidamente, definiremos un `nuevo ámbito`, para ello elegimos el botón `Nuevo Ámbito` teniendo seleccionado nuestro dominio.

![Nuevo Ámbito](./images/ambito-nuevo.png)

* Escribimos el intervalo de direcciones que distribuye el ámbito.

![Intervalo IP](./images/intervalo-ip.png)

* Tras esto, marcamos el intervalo de direcciones IP qu deseemos excluir.

![Excluir IP](./images/excluir.png)

![Concesión de DHCP](./images/concesion.png)

* Agregamos una dirección IP para un enrutador (Puerta enlace) usado por clientes.

![Puerta de enlace](./images/puerta-enlace.png)

* Configurar nombre de dominio.

![](./images/dns.png)

* Para finalizar activamos el ámbito.

![Activar ámbito](./images/activardh.png)

* Reservamos un cliente con la MAC.

![Reservar por MAC](./images/reserva-mac.png)

---

## 3. Comprobar funcionamiento

Ahora comprobamos que todo funciona correctamente.

![Conexión por DHCP](./images/.png)

![](./images/conectado1.png)

---

## 4. Crear nuevo ámbito

Ahora crearemos un nuevo ámbito compatible con el anterior.

**Primer paso**

![](./images/intervalo-ip2.png)

**Segundo paso**

![](./images/excluir2.png)

**Tercer paso**

![](./images/dns2.png)

---

## 5. Superámbito

Creamos un super ámbito en el que estén los dos ámbitos incluidos y lo desactivamos para comprobar que DHCP deja de prestar servicio en ambos ámbitos.

![](./images/agregar-superambito.png)

![](./images/conectado.png)
