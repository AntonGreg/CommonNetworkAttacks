# CommonAttacks

## Ataque de fuerza bruta

Definición:

Un **ataque de fuerza bruta** es un método de prueba y error utilizado para decodificar datos confidenciales. Las aplicaciones más comunes para los **ataques de fuerza bruta** son descifrar contraseñas y descifrar claves de cifrado.

## ¿A que afecta?

Afecta principalmente a las **contraseñas de los usuarios**, por lo que se vería gravemente comprometida la privacidad de los mismos ya que estos ataques suelen hacerlos usuarios no autorizados para obtener información.

## ¿Cómo prevenir?

Se puede prevenir el ataque por fuerza bruta usando **contraseñas fuertes** (con números y caracteres especiales).

Los **bloqueos de cuenta con demoras progresivas** bloquean una cuenta solo durante un período de tiempo determinado después de un número designado de intentos de inicio de sesión fallidos por lo que las herramientas automatizadas de ataque de fuerza bruta no serán tan útiles. 

Los **CAPTCHA** también previenen de muy buena forma estos ataques ya que así hace que los bots automáticos sean ineficaces al tener que resolver una serie de valores gráficos.

# Envenenamiento de DNS

Definición:

El envenenamiento de caché de DNS consiste en introducir información falsa en una caché DNS, para que las consultas de DNS devuelvan una respuesta incorrecta y se dirija a los usuarios a sitios web equivocados. El envenenamiento de caché de DNS también se conoce como "suplantación de DNS"

## ¿A qué afecta?

En este ataque, un pirata informático falsifica la información **que** recibe su ordenador cuando le pide la dirección IP de un sitio web. Esto puede hacer **que** su ordenador acceda a un sitio equivocado o incluso **que** sea redirigido a un sitio malicioso. 

## ¿Cómo prevenir?

Hay dos áreas afectadas por el envenenamiento de DNS: del lado del cliente y del lado del **servidor**. 

Empecemos por lo que hace Internet en su conjunto en el lado del servidor:

El uso de las extensiones de seguridad del sistema de nombres de dominio (DNSSEC)(https://www.dnssec.net/). Se trata de una tecnología diseñada para combatir el envenenamiento del DNS y, en términos sencillos, pone en marcha diferentes niveles de verificación.

En profundidad, DNSSEC utiliza la «criptografía de clave pública» como verificación. Se trata de una forma de certificar que los datos son auténticos y fiables. Se almacena junto con el resto de la información del DNS y el servidor recursivo la utiliza para comprobar que ninguna de las informaciones que recibe ha sido alterada.

Por parte del lado del **cliente** se pueden realizar distintas acciones:



- Utilizar el cifrado de extremo a extremo para cualquier solicitud y respuesta. Los certificados Secure Sockets Layers (SSL). hacen un buen trabajo aquí.
- Utiliza herramientas de detección de spoofing. Estas pueden escanear los paquetes de datos recibidos antes de enviarlos. Estas escanean los paquetes de datos recibidos antes de enviarlos. Esto mitiga cualquier transferencia de datos maliciosa.
- Aumentar los valores de tiempo de vida(TTL) de tu caché DNS ayudará a eliminar las entradas maliciosas antes de que puedan llegar a los usuarios finales.
- Debes tener una buena estrategia de DNS, DHCP e IPAM (DDI). Esto consiste en tu estrategia de DNS, el Protocolo de Configuración Dinámica de Host y la Gestión de Direcciones IP. Se trata de un proceso complejo pero necesario, gestionado por administradores de sistemas y expertos en seguridad de servidores.

Como **usuario final**, hay algunas cosas más que puedes hacer para ayudar a prevenir el envenenamiento y la suplantación de identidad:

- Utiliza una [red privada virtual (VPN)](https://kinsta.com/es/blog/proxy-vs-vpn/#what-is-a-virtual-private-network-vpn), ya que tus datos estarán encriptados de extremo a extremo. También podrás utilizar servidores DNS privados, también con encriptación de extremo a extremo.
- Toma sencillas precauciones, como no hacer clic en enlaces no reconocidos y realizar análisis de seguridad periódicos.
- [Limpiar la caché de DNS](https://kinsta.com/es/base-de-conocimiento/vaciar-cache-dns/) con regularidad también elimina los datos maliciosos de tu sistema. Es algo que lleva unos segundos y es sencillo de llevar a cabo.
