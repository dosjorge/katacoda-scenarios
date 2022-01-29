Una vez instalado `cloudflared` es posible ejecutar el servicio web a compartir.  En este caso se usará el _echo server_[^1] `http-echo`. 

[^1]: Un _echo server_ (en español _servidor de eco_) es una aplicación que se utiliza para probar si la conexión entre un cliente y un servidor es exitosa. En este caso el programa imprime el texto enviado por el cliente y envía al cliente un texto de prueba predefinido.

Entonces, debe instalarse el _echo server_.
```sh
curl -sL https://github.com/hashicorp/http-echo/releases/download/v0.2.3/http-echo_0.2.3_linux_amd64.tar.gz | sudo tar xzpC /usr/local/bin
```{{execute T1}}

Luego podemos ejecutarlo
```sh
http-echo -listen=:8080 -text="hola mundo"
```{{execute T2}}

Finalmente podemos probarlo
```sh
curl http://127.0.0.1:8080
```{{execute T1}}

En el siguiente módulo se ejecutará `cloudflared` para compartir el servicio.
