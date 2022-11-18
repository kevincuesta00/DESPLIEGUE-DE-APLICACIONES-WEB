#  Tema 3: Apache

## Como instalar apache en ubuntu 
* Instalar apache 
Lo primero que tenemos que hacer es actualizar los paquetes locales de ubuntu.

>sudo apt update
>
>sudo apt upgrade


Una vez actualizada procedemos a instalar el servidor apache,

>sudo apt install apache2
## Configurar firewall

Antes de probar Apache, es necesario modificar los ajustes de firewall para permitir el acceso externo a los puertos web predeterminados.

Durante la instalación, Apache se registra con UFW para proporcionar algunos perfiles de aplicación que pueden utilizarse para habilitar o deshabilitar el acceso a Apache a través del firewall.

Con este comando enumeramos los perfiles de aplicacion.

>sudo ufw app list

captura

* Apache: este perfil abre solo el puerto 80 (tráfico web normal no cifrado)
* Apache Full: este perfil abre el puerto 80 (tráfico web normal no cifrado) y el puerto 443 (tráfico TLS/SSL cifrado)
* Apache Secure: este perfil abre solo el puerto 443 (tráfico TLS/SSL cifrado)

Se recomienda habilitar el perfil más restrictivo, con el siguiente comando: 

>sudo ufw allow 'Apache'

Verifica el cambio con el siguiente comando:

>sudo ufw status

captura










