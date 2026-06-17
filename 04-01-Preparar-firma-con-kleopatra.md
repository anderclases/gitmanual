# Preparar firma con Kleopatra
En este manual se explica cómo configurar la firma generando las claves directantamente desde Kleopatra. 

## 1️⃣ Generar la clave GPG en Kleopatra
- archivo > Nuevo par de OpenPGP
- El email debe de coincidir con el email de github.

## 2️⃣ Obtener el ID de la clave (Key ID)
Click derecho detalles y copia la huella digital.

## 3️⃣ Configurar Git para usar esa clave
```bash
git config --global user.signingkey ID_HUELLA_DIGITAL
git config --global commit.gpgsign true
```

## 4️⃣ Decirle a Git que use GPG (Windows + Kleopatra)
(Normalmente no va a ser necesario, pero asegura que no haya conflictos con algún otro cliente GPG instalado)
```bash
git config --list
git config --global gpg.program "PAHT_DE_GPG"
# Path de windows
C:/Program Files (x86)/GnuPG/bin/gpg.exe
# Path de git bash
C:\Program Files (x86)\GnuPG\bin\gpg.exe
```

Tras estos dos comandos el sistema será capaz de realizar las firmas de nuestros commits. Para que github reconozca nuestra firma debemos subirla a nuestra cuenta.

## 5️⃣ Exportar la clave PÚBLICA y subirla a GitHub

En Kleopatra:
- Click derecho en tu clave
- Exportar
- Guarda el archivo .asc

Luego en GitHub:
- Settings → SSH and GPG keys
- New GPG key
- Abre el .asc con un editor de texto
- Copia todo el contenido y pégalo
- Guarda
