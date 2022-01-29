# Instalar `cloudflared`

Para conectar su infraestructura local a Cloudflare debe instalar `cloudflared`, que es un demonio[^1] de [código abierto](https://github.com/cloudflare/cloudflared) que cumple esta función. Recuerde que también puede consultar las instrucciones oficiales de instalación en [Cloudflare Docs](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/install-and-setup/installation).

## Instalar llave PGP de Cloudflare

Para poder instalar `cloudflared` en Ubuntu antes debemos instalar el repositorio oficial de Cloudflare. Para ello, primero debemos agregar la llave pública PGP a la lista de llaves de confianza del sistema para la autentificación de programas instalados.

```sh
curl -sL 'https://pkg.cloudflare.com/cloudflare-main.gpg' | sudo apt-key add -
```{{execute}}

## Instalar repositorio de Cloudflare

Luego podemos agregar el repositorio de Cloudflare al sistema.

```sh
sudo add-apt-repository "deb https://pkg.cloudflare.com/ $(lsb_release -sc) main"
```{{execute}}

## Instalar `cloudflared`

Finalmente podemos instalar `cloudflared`.

```sh
sudo apt install cloudflared
```{{execute}}

[^1]: Un demonio (en inglés _daemon_) es un programa que se ejecuta en segundo plano y supervisa el sistema o proporciona funcionalidad a otros procesos. Fuente: [daemon (7)](https://man7.org/linux/man-pages/man7/daemon.7.html#:~:text=A%20daemon%20is%20a%20service%20process%20that%20runs%20in%20the%20background%20and%0A%20%20%20%20%20%20%20supervises%20the%20system%20or%20provides%20functionality%20to%20other%0A%20%20%20%20%20%20%20processes.).
