
# Instalación y Configuración de un Servidor de Correo Electrónico en Linux

---

## 1. Postfix

### 1.1. Instalación

Comenzaremos instalando `Postfix` que es el servicio `SMTP en Linux` con:
* `sudo apt install postfix`.

![](./images/1-inst-post.png)

Escogemos la instalación como `Sitio de Internet`

![](./images/2-internet.png)

Creamos nuestro dominio de correo.

![](./images/3-dom-correo.png)

Y terminada la instalación comprobamos que el puerto **SMTP** esta activo y a la escucha con el comando `netstat -utap`.

![](./images/4-escucha-smtp.png)

### 1.2. Comprobación

Creamos dos usuarios y enviamos un correo por `telnet` para comprobar el envío y recepción de mensajes de correo.

![](./images/5-sent-mail.png)

![](./images/6-comp-mail.png)

---

## 2. Evolution

### 2.1. Instalación

![](./images/7-evolution.png)

![](./images/8-evolution-graf.png)

### 2.2. Configuración

![](./images/9-hosts.png)

![](./images/10-ident.png)

![](./images/11-conf-iden.png)

### 2.2. Comprobación

![](./images/12-comp-mensajes.png)

![](./images/13-autent.png)

![](./images/14-mail-recibido.png)

---

## 3. IMAP

### 3.1. Instalación

![](./images/15.png)

### 3.2. Comprobación

![](./images/16.png)

---

## 4. Squirrel

### 4.1. Instalación

![](./images/17.png)

### 4.2. Configuración

![](./images/18.png)

### 4.3. Comprobación

![](./images/19.png)

![](./images/20.png)

![](./images/21.png)

**Comprobando envío a `envpost`**

![](./images/22.png)

![](./images/23.png)

---

## 5. POP3

### 5.1. Instalación

![](./images/24.png)

![](./images/25.png)

---
