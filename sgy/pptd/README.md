
# VPN en Linux con PPTP

---

## Configuración IP estática

Comenzamos poniendo la IP estática en fichero `/etc/network/interfaces`.

## Instalando PPTP

Para instalarlo, lo hacemos con **zypper**.

![](./images/pptpd.png)

## Configuración

Ahora modificaremos 5 ficheros:
* /etc/ppp/chap-secrets

![](./images/chap-secrets.png)

* /etc/ppp/options

![](./images/ppp-options.png)

* /etc/ppp/pptpd-options

![](./images/pptpd-options.png)

* /etc/pptpd.config

![](./images/ppptpd-config.png)

* /etc/rc.local

![](./images/rc-local.png)

## Comprobación

![](./images/comp.png)
