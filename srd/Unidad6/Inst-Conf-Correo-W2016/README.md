
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

Ahora vamos a `Propiedades` del `SMTP` y configuramos lo siguiente en el apartado **General**:

| Dirección IP | Limitar conexiones | Habilitar registro | Formato de registro activo |
| :----------: | :----------------: | :----------------: | :------------------------: |
| 172.19.15.21 | 50                 | SI                 |   Registro Extendido W3C   |

![](./images/.png)

Después, vamos al apartado **Acceso** y configuramos la autenticación anónima y el envío de mensajes dentro de nuestra red local.

> Para hacer esto, aceptamos la conexión al servidor y la retransmisión de mensajes a todos los equipos menos a una IP, la que nosotros queramos, en mi caso `172.19.15.32`

<table>
  <tr>
    <th rowspan="1">Control de conexión</th>
    <th>Control de acceso</th>
  </tr>
  <tr>
    <th></th>
    <th></th>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td></td>
  </tr>
</table>

##
