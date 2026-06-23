# Setup Guide

## Step 1: Create Virtual Machine

* Login to VMware Cloud Director.
* Navigate to Virtual Machines.
* Create a new VM.

Configuration:

* 4 vCPU
* 8 GB RAM
* 38 GB Storage
* Ubuntu 22.04 LTS

---

## Step 2: Login to VM

Open VM Console and login as root.

---

## Step 3: Update Server

```bash
apt update
apt upgrade -y
```

---

## Step 4: Install Apache

```bash
apt install apache2 -y
```

Check service:

```bash
systemctl status apache2
```

Enable service:

```bash
systemctl enable apache2
```

---

## Step 5: Verify Web Server

```bash
ss -tulnp | grep :80
```

---

## Step 6: Remove Default Page

```bash
cd /var/www/html

rm index.html
```

---

## Step 7: Create Website

```bash
nano index.html
```

Paste the HTML code.

---

## Step 8: Restart Apache

```bash
systemctl restart apache2
```

---

## Step 9: Access Website

```text
http://49.50.92.79
```

---

## Outcome

Successfully hosted a static website on Ubuntu Virtual Machine using VMware Cloud Director.
