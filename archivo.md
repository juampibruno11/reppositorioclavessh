 Primero, se genera la clave SSH desde la terminal utilizando el comando ssh-keygen -t ed25519 -C "correo@ejemplo.com". Este proceso crea dos archivos: una clave privada (que no debe compartirse) y una clave pública (que se utilizará para GitHub). Se acepta la ubicación por defecto y, opcionalmente, se puede agregar una contraseña.
Luego, se visualiza la clave pública con el comando cat ~/.ssh/id_ed25519.pub y se copia completamente el contenido que aparece en pantalla.
A continuación, se vincula la clave con GitHub ejecutando gh auth login, seleccionando GitHub.com, eligiendo el protocolo SSH y autorizando el uso de la clave generada.
Después, se clona el repositorio desde GitHub con git clone git@github.com:usuario/repositorio.git y se accede a la carpeta del proyecto con cd repositorio.
Dentro del repositorio, se crea el archivo utilizando touch archivo.md, se agrega con git add . y se realiza un commit con git commit -m "mensaje".
Finalmente, se sube el archivo al repositorio con git push --set-upstream origin main, dejando conectada la rama local con la remota para futuros envíos.
Para actualizar el archivo más adelante, se edita con nano archivo.md, se guarda y se vuelve a ejecutar git add, git commit y git push.
