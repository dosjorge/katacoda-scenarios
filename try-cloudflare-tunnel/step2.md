Una vez instalado `cloudflared` es posible ejecutar el servicio web a compartir.  En este caso se usará el _echo server_<sup id="dagger-1">[1](#footnote-1)</sup> `http-echo`. 

En primer lugar debe instalarse el _echo server_.

```sh
curl -sL https://github.com/hashicorp/http-echo/releases/download/v0.2.3/http-echo_0.2.3_linux_amd64.tar.gz | sudo tar xzpC /usr/local/bin
```{{execute T1}}

Luego puede ser ejecutado.

```sh
http-echo -listen=:8080 -text="hola mundo"
```{{execute T2}}

Finalmente puede probarlo.

```sh
curl http://127.0.0.1:8080
```{{execute T1}}

En el siguiente módulo se ejecutará `cloudflared` para compartir el servicio.

<b id="footnote-1">1</b> Un _echo server_ (en español _servidor de eco_) es una aplicación que se utiliza para probar si la conexión entre cliente y servidor es exitosa. En este caso el servidor imprime en la terminal la [solicitud HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages#http_requests) enviada por el cliente y envía al cliente un texto de prueba predefinido, en este caso _hola mundo_. [↩](#dagger-1)
