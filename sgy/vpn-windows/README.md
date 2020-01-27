
# VPN en Windows Server

---

## 1. Configuración Servidor - Windows 2016 Server

Antes que nada, ponemos la IP estática, configurada manualmente.

Ahora instalaremos `VPN` en el servidor, para ello, tenemos que ir dentro de `Administrador del servidor`:
* Administrar:
  * Agregar roles y características

* Instalamos `Acceso remoto`

![](./images/cliente-1-access.png)

![](./images/cliente-2-direct-access.png)

Ahora configuraremos el `Enrutamiento y acceso remoto`:

![](./images/enrutamiento.png)

Le damos a Siguiente:

![](./images/cliente-3-enrutamiento.png)

![](./images/cliente-4-acceso-remoto.png)

Para finalizar la configuración en Windows 2016 Server, tendremos que crear un usuario de Active Directory, en mi caso **alejandro**, y le concedemos *Permitir acceso* en `Permiso de acceso a redes` en el apartado **Marcado**.

![](./images/usuario-alejandro.png)

---

## 2. Comprobación Cliente - Windows10

Comprobamos que se puede conectar desde el cliente Windows 10.

![](./images/vpn-correcto.png)

Para finalizar, comprobamos que tenemos acceso a internet haciendo un `ping 8.8.8.8`

![](./images/internet.png)
