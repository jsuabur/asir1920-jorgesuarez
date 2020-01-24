
# Instalación y Configuración de Servicios de Correo Electrónico en Windows 2016 Server

---

## 1. Instalación - Servidor SMTP

En el `Administrador del servidor`, entramos en `Agregar roles y características`, una vez ahí seguimos los siguientes pasos:

**1º Paso**

![](./images/1-inst-smtp.png)

**2º Paso**

![](./images/2-inst-smtp.png)

**3º Paso**

![](./images/3-inst-smtp.png)

**4º Paso**
Seleccionar `Servidor SMTP`.

![](./images/4-inst-smtp.png)

**Último paso**

Ejecutar la instalación.

![](./images/5-instalando.png)

## 2. Configuración - Servidor SMTP

Ahora configuraremos el `Servidor SMTP`, para ello vamos a `Administrador de Internet Information Services (IIS) 6.0`.

![](./images/6-iis-60.png)

Ahora vamos a `Propiedades` del `SMTP` y configuramos lo siguiente:

| Dirección IP | Limitar conexiones | Habilitar registro | Formato de registro activo |
| :----------: | :----------------: | :----------------: | :------------------------: |
| 172.19.15.21 | 50                 | SI                 |   Registro Extendido W3C   |

##
