
# Proxy

---

## 1. Configuración

### 1.1. Package Manager

Primero buscaremos e instalaremos `squid`.

![](./images/1-proxy-squid.png)

### 1.2. Squid Proxy Server

En el apartado `Local Cache` modificamos lo siguiente:

![](./images/2-squid-hard-disk.png)

En el apartado `General` modificamos lo siguiente:

![](./images/3-squid-general.png)

![](./images/4-logging.png)

### 1.3. Status

Comprobamos en `Services`.

![](./images/5-status-services.png)

### 1.4. Certificate Manager

En el apartado `CAs` modificamos lo siguiente:

![](./images/6-create-ca.png)

![](./images/7-comp-cert.png)

### 1.5. Squid Proxy Server

![](./images/8-ssl-man.png)

En el apartado `Antivirus` modificamos lo siguiente:

![](./images/9-antivirus.png)

## 2. Comprobación

En el apartado `Blacklist` añadiremos alguna página web para comprobar que funciona.

![](./images/10-backlist.png)

Comprobamos intentando acceder a estas páginas.

![](./images/11-marca-block.png)

![](./images/12-https.png)
