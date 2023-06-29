# configurarGitEnLinux
Tutorial que se usó:
https://stackoverflow.com/questions/8588768/how-do-i-avoid-the-specification-of-the-username-and-password-at-every-git-push

## Para realizar la configuración primero se debe generar una llave 

```sh
cd ~                 #Se para en el home
ssh-keygen -t rsa    #Se genera la llave o se revisa si ya existe
vim .ssh/id_rsa.pub  #Si el archivo existe se copia toda la línea quitando los espacios en blanco
```
## Adición de la llave a github

Se va a éste link:

https://github.com/settings/ssh

Y se genera la llave en donde dice 'New SSH Keygen', se le da un nombre y se pega los valores que vienen del archivo '.ssh/id_rsa.pub'

## Forma de clonar los repositorios
Luego de que se configura la nueva llave, ahora se deben clonar los archivos con ssh.

```sh
git clone git@github.com:etorresm/xxxyyyyy
```
