# Instalar `cloudflared`

Para conectar su infraestructura local a Cloudflare debe instalar `cloudflared`, que es un demonio<sup id="dagger-1">[1](#footnote-1)</sup> de [código abierto](https://github.com/cloudflare/cloudflared) que cumple esta función.

Para poder instalar `cloudflared` en Ubuntu primero se debe instalar el repositorio oficial de Cloudflare. Si desea instalar el demonio en otros sistemas operativos puede consultar las instrucciones oficiales de instalación en [Cloudflare Docs](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/install-and-setup/installation).

## Instalar llave PGP de los repositorios de Cloudflare

En primer lugar agregue la llave pública PGP a la lista de llaves de confianza del sistema para la autentificación de programas instalados.

```sh
curl -sL 'https://pkg.cloudflare.com/cloudflare-main.gpg' | sudo apt-key add -
```{{execute}}

## Instalar repositorio de Cloudflare

Luego agregue el repositorio de Cloudflare al sistema.

```sh
sudo add-apt-repository "deb https://pkg.cloudflare.com/ $(lsb_release -sc) main"
```{{execute}}

## Instalar `cloudflared`

Finalmente puede instalar `cloudflared`.

```sh
sudo apt install cloudflared
```{{execute}}

<b id="footnote-1">1</b> Un demonio (en inglés _daemon_) es un programa que se ejecuta en segundo plano y supervisa el sistema o proporciona funcionalidad a otros procesos. Fuente: [daemon (7)](https://man7.org/linux/man-pages/man7/daemon.7.html#:~:text=A%20daemon%20is%20a%20service%20process%20that%20runs%20in%20the%20background%20a  nd%0A%20%20%20%20%20%20%20supervises%20the%20system%20or%20provides%20functionality%20to%20other%0A%20%20%20%20%20%20%20processes.). [↩](#dagger-1)
