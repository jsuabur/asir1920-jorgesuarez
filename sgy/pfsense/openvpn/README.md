
# OpenVPN

---

![](./images/.png)

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

![](./images/.png)

![](./images/.png)

![](./images/.png)

![](./images/.png)

![](./images/.png)
