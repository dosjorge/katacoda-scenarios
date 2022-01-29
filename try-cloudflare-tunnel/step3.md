Finalmente podemos ejecutar `cloudflared` para compartir el servicio en internet.

```sh
cloudflared tunnel --url http://127.0.0.1:8080
```{{execute}}

Tras inicializarse, `cloudflared` entregará una URL con la que cualquiera en la Internet puede visitar el servicio web ejecutado previamente.
