# Práctica . Git


#### GitHub
1. [GitHub](https://github.com/) es una plataforma de desarrollo colaborativo para alojar proyectos utilizando el sistema de control de versiones Git.
Cree una cuenta en [GitHub](https://github.com/) y configure su perfil de esa cuenta de modo que incluya una imagen (fotografía) en la que se le reconozca y haga que la cuenta de e-mail asociada sea la dirección institucional o su alias.
Para la configuración de esa cuenta se le recomienda usar su nombre real, puesto que sus repositorios de código en GitHub
pasarán a formar parte de su curriculum profesional.


#### git y GitHub
2. Compruebe que `git` está instalado en su máquina:
```
$ git --version
```
Si nunca ha usado Git, tal vez le interese conocer los
[conceptos básicos](https://docs.github.com/es/get-started/using-git/about-git)
de la herramienta.
Si quiere un tutorial rápido sobre los principales comandos que necesitará, 
[esta](https://www.linux.com/topic/desktop/introduction-using-git/)
puede ser una buena referencia para comenzar.
Hay mucha más documentación sobre Git en línea:
* [GitHub Guides](https://docs.github.com/es)
* [Cheat Sheet for Common Operations](https://training.github.com/downloads/github-git-cheat-sheet.pdf)
* [Command Reference](https://git-scm.com/docs)
* [Online Simulator/Tutorial](https://learngitbranching.js.org/?locale=es_ES)
Con posterioridad a esta práctica, revise esta documentación.

3. Consiga que se pueda subir código desde su máquina virtual hacia su cuenta GitHub sin necesidad de autentificación. 
Consulte para ello las instrucciones
[Adding a new SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)
En su máquina virtual ejecute los siguientes comandos para generar e instalar una clave SSH (donde `alu...edu.es` es la cuenta que haya utilizado para registrarse en GitHub):
```
$ ssh-keygen -t ed25519 -C "alu...edu.es"
$ eval "$(ssh-agent -s)"
$ ssh-add ~/.ssh/id_ed25519
$ cat ~/.ssh/id_ed25519.pub
```
  - El primer comando le preguntará dónde generar la clave y si desea darle una contraseña. En ambos casos puede pulsar *Enter* sin escribir ningún valor para mantener los valores por defecto.
  - El cuarto comando mostrará por pantalla todo el contenido de la clave generada, que debería ser una línea que comienza por `ssh-ed25519` y termina con su cuenta de correo electrónico. Seleccione y copie la línea completa.
  - En su cuenta de GitHub, haga clic en el icono con su foto en la esquina superior derecha y luego en *Settings.* En la columna izquierda, haga clic *SSH and GPG keys* del apartado *Access* y luego en el botón *New SSH key.*
  - Dé a su nueva clave el nombre que prefiera (por ejemplos, "Informática Básica 2025/2026") y pegue el contenido de la clave generada. Pulse en "Add SSH Key" y su cuenta GitHub quedará enlazada con su máquina virtual.

4. Cree un directorio `practicas` y clone en él un repositorio git:
```
cd
mkdir practicas
cd practicas
git clone git@github.com:Repositorio_en_github.git Nombre_directorio_en_mi_maquina
```

```
para conectarse a la máquina virtual.
