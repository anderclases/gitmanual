# Firmar commits en Git

GPG (GNU Privacy Guard), es una herramienta de seguridad en comunicaciones electrónicas y su utilidad es la de cifrar y **firmar digitalmente**, siendo además multiplataforma.

GPG utiliza el **cifrado asimetrico** o *criptografía de clave pública* para que los usuarios puedan comunicarse de un modo seguro. En un sistema de claves públicas cada usuario posee un par de claves, compuesto por una "clave privada" y una "clave pública". Cada usuario debe mantener su clave privada secreta; no debe ser revelada nunca. La clave pública se puede entregar a cualquier persona con la que el usuario desee comunicarse.

Git utiliza un sistema de firma asimétrica para firmar los commmit.

**¿En la práctica que significa esto?**

Nosotros firmamos con nuestra clave privada que está ubicada en nuestro ordenador. Github al tener nuestra clave publica guardada puede comporbar que el commit ha sido firmado con esa clave privada.

Una buena metafora de la criptografía asimetrica es la de la llave y el candado.

![Ejemplo criptografia asimetrica](./images/firma/Cripto_asimetrica.png)
