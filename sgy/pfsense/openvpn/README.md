
# OpenVPN

---

## 1. Configuración - Panel de Control PFsense

### 1.1. Certificate Manager

En el apartado `CAs` añadimos un certificado con las siguientes características.

![](./images/openvpn.png)

![](./images/2-create-edit.png)

![](./images/3-comp-create.png)

Ahora vamos al apartado `Certificates` y lo rellenamos de la siguiente forma:

![](./images/4-certificate-1.png)

![](./images/4-atributtes-2.png)

![](./images/5-comp-cert.png)

### 1.2. Wizards

**Type of Server:** `Local User Access`

![](./images/6-wizard.png)

![](./images/7-cert-auth.png)

![](./images/8-cert-vpn.png)

![](./images/9-remote.png)

![](./images/10-tunnel.png)

![](./images/11-firewall.png)

### 1.3. OpenVPN

En el apartado `Servers` comprobamos que se ha creado correctamente.

![](./images/12-comp-opnvpn.png)

Y ahora creamos un cliente en el apartado `Clients`.

![](./images/13-client.png)

![](./images/14-user-auth.png)

![](./images/15-advanced-congf.png)

![](./images/16-comp-client.png)

### 1.4. Package Manager

En el apartado `Available Packages` buscamos el paquete ***openvpn-client-export*** y lo instalamos.

![](./images/17-sstem.png)

---

## 2. Comprobación

Comprobamos con el comando `tracert 8.8.8.8`.

![](./images/18-conecta.png)
