# Omada-SW-on-PC
Install Omada Software on any PC &amp; Raspberry-PI

* No package in regular repositories only AUR 😉.

### 1. Installation

1. Searching method:

`paru omada`

* Choose Nº1 = `omada-controller` vers. "5.13.23-1" or higher &&
* choose `7) mongodb44-bin` or higher && confirm like [here explained](https://aur.archlinux.org/packages/omada-controller)

2. Alternative Version for 32-Bit-CPU

```
paru -S --needded --noconfirm omada-controller-v3
```

3. DEB-64-Bit
* Omada [Download-Page](https://www.tp-link.com/de/support/download/omada-software-controller/#Controller_Software)
* Omada [Original Instructions](https://www.tp-link.com/de/support/faq/3272/)
* Alternative Instructions 4 [Ubuntu 20.04](https://www.crosstalksolutions.com/tp-link-omada-installation-on-ubuntu-20-04/)

4. [DEB-32-Bit](https://github.com/JsBergbau/Omada-SDN-Controller-mongodb-Raspberry-PI/blob/main/README.md)

**Note:** this should running also on 32-Bit CPU's like "RasPy"

5. [Docker-Omada-Controller](https://github.com/mbentley/docker-omada-controller)



### 2. Enable & Start Service like [here](https://www.redhat.com/sysadmin/linux-systemctl-manage-services) & [here explained](https://aur.archlinux.org/packages/omada-controller)

1. The enable subcommand doesn't start a service, it only marks it to start automatically at boot. To enable and start a service at the same time, use the --now option:

* Full command:

```
sudo systemctl enable --now omada-controller
```

* Check service is enable & running

```
sudo systemctl list-units | grep omada
```

* Output:

```
omada-controller.service >>>> loaded active running   Omada SDN Controller
```

* Alternative or extensive checking:

```
sudo systemctl status omada-controller
```



2. Activate Service in Artix-Linux (OpenRC)

```
sudo rc-update add omada-controller.service  default

sudo rc-service omada-controller.service start 
```

### 3. Start Omada

* Syntax: `http://[server IP]:8088`

1. Search your server IP-Address with:

`ip --color=auto a`

* Note and/or copy/paste IP-Address!

2. The full Address in my case:

```
http://192.168.178.20:8088
```

* Effective or final Address:

```
https://192.168.178.20:8043/413c344081e085babdc1a19aff4a0ad4/login
```

* **Picture of first start 🟰 Login:**

![](_2024-02-21_17-01-30_0001.jpeg)



✅ **Done**❗️ **Enjoy** 😄

