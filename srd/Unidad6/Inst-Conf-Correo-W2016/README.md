
# Instalación y Configuración de Servicios de Correo Electrónico en Windows 2016 Server

---

## 1. Servidor SMTP

### 1.1. Instalación

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

### 1.2. Configuración

Ahora configuraremos el `Servidor SMTP`, para ello vamos a `Administrador de Internet Information Services (IIS) 6.0`.

![](./images/6-iis-60.png)

Ahora vamos a `Propiedades` del `SMTP` y configuramos lo siguiente en el apartado **General**:

| Dirección IP | Limitar conexiones | Habilitar registro | Formato de registro activo |
| :----------: | :----------------: | :----------------: | :------------------------: |
| 172.19.15.31 | 50                 | SI                 |   Registro Extendido W3C   |

![](./images/7-general.png)

Después, vamos al apartado **Acceso** y configuramos la autenticación anónima y el envío de mensajes dentro de nuestra red local.

> Para hacer esto, aceptamos la conexión al servidor y la retransmisión de mensajes a todos los equipos menos a una IP, la que nosotros queramos, en mi caso `172.19.15.52`


<table>
  <tr>
    <th colspan="2">Control de conexión</th>
    <th>Control de acceso</th>
  </tr>
  <tr>
    <th>Conexión</th>
    <th>Equipo</th>
    <th>Autenticación</th>
  </tr>
  <tr>
    <td>Todo excepto la lista que aparece a continuación</td>
    <td>Un único equipo</td>
    <td rowspan="2">Acceso anónimo</td>
  </tr>
  <tr>
    <td colspan="2">Dirección IP 172.19.15.52</td>
  </tr>
</table>

![](./images/8-unico-pc.png)

![](./images/9-denegado.png)

![](./images/10-acc-anonimo.png)

## 1.3. Nuevo dominio SMTP

Antes de nada, comprobamos que existe el dominio predeterminado de Active Directory.

![](./images/11-AD-predet.png)

Después creamos un dominio tipo alias para disponer de cuentas en otro dominio.

![](./images/12-dominio-new.png)

**1º Paso**

![](./images/13-smtp-alias.png)

**2º Paso**

![](./images/14-alias-suarez.png)

**Comprobación**

![](./images/15-creado.png)

Ahora vamos a ver si se han creado correctamente las carpetas de correo en `C:\Inetpub\mailroot`:

![](./images/16-mailroot.png)

## 1.4. Correos

En el cliente Windows 7, comprobamos mediante `nslookup` el acceso al nuevo nombre DNS creado en el servidor de correo.

![](./images/17-nslookup.png)

Ahora, enviaremos algunos correos hacia las cuentas y comprobamos el envío y carpetas mailroot. Las carpetas tienen distintas funciones que son:
* Queue -> Mensajes en cola
* Badmail -> Mensajes para desconocidos
* Drop -> Mensajes entregados

![](./images/18-prueba-anon.png)

---

# 2. hMailServer

* Antes que nada desinstalamos el servicio `SMTP` de Windows 2016 Server.

![](./images/20-desinst.png)

![](./images/21-eliminando.png)

Ahora descargamos e instalamos en **Windows 2016 Server** el servidor de correo `hMailServer`.

![](./images/23-hmail.png)

![](./images/24-hmail-inst.png)

> Para que funcione correctamente debemos instalar la característica `.NET Framework 3.5`.

![](./images/25-net35.png)

![](./images/26-instalado-hmail.png)
