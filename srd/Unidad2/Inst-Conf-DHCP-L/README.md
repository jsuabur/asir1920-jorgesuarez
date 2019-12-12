
# Instalación y Configuración DHCP Linux

---

## 1. Instalación DHCP

Primero instalamos el paquete `isc-dhcp-server` mediante el gestor de paquetes `apt-get`:

![](./images/instalar-dhcp.png)

---

## 2. Configuración DHCP

Ahora configuraremos la interface en el fichero `/etc/default/isc-dhcp-server` modificando la siguiente línea:

```bash
INTERFACES="enp0s3"
```

![](./images/interfaces.png)

### 2.1. Copia de seguridad

Antes de editar el fichero, haremos una copia de seguridad del mismo, para prevenir errores o problemas.

![](./images/copy-dhcp-conf.png)

### 2.2. Configuración

Ahora configuraremos el fichero con las opciones correspondientes.

![](./images/domain-server.png)

---
