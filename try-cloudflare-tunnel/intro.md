[Cloudflare Tunnel](https://www.cloudflare.com/es-la/products/tunnel/) le brinda una forma segura de conectar sus recursos a Cloudflare sin abrir puertos en su servidor.  Con Tunnel, no envía tráfico a cualquiera en la internet de forma directa; en cambio, un demonio en su servidor (`cloudflared`) crea conexiones salientes a los [_edge servers_](https://www.cloudflare.com/learning/cdn/glossary/edge-server/) de Cloudflare. De esta forma, su servidor puede atender tráfico a través de Cloudflare sin necesidad de una IP enrutable al público.

Este servicio puede ser muy util para demostrar sitios web en desarrollo a potenciales clientes u otros usos que no sean de producción.  Para entornos de producción puede utilizar [Cloudflare for Teams](https://katacoda.com/dosjorge/scenarios/cloudflare-tunnel)

, si bien el servicio es gratuito, precisa de dos cosas:

1. [Registrarse en Cloudflare](https://dash.cloudflare.com/sign-up)
2. [Agregar](https://www.youtube.com/watch?v=7hY3gp_-9EU) o [comprar](https://developers.cloudflare.com/registrar/get-started/register-domain) un [dominio web](https://www.cloudflare.com/learning/dns/glossary/what-is-a-domain-name/) en Cloudflare

El costo de un dominio .com en Cloudflare es de USD 8.57 (aproximadamente 7 000 CLP) al año al 29 de enero del 2022.

las instrucciones para ello están disponibles en el escenario [cloudflare-tunnel-production]().


En este escenario de Katacoda aprenderá a instalar y usar `cloudflared` en Ubuntu.
