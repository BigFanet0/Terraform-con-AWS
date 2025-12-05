# Terraform-con-AWS

Antes de descargar AWS y TerraForm, siempre nos aseguramos en actualizar el sistema.

*sudo apt update*

*sudo apt upgrade -y*

Como estamos en un entorno Linux(Ubuntu 24.04 en mi caso) las installaciones y configuraciones las haremos desde el CLI(Terminal). Mas adelante tendremos que extraer ficheros zip que necesitemos para el correcto funcionamiento de nuestro servicio. 
Una herramienta clara para extraer archivos zip en linux es el "unzip" asi que procedemos a instalarlo.

*sudo apt install zip unzip -y*

# Instalacion de AWS CLI
A Continuacioón, luego de instalar el "unzip" vamos a proceder a descargar e instalar AWS CLI. Para ello ejecutamos los siguiente:

*curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"*

 <img width="1469" height="128" alt="imagen" src="https://github.com/user-attachments/assets/f26a6cb4-677b-4c87-978c-2dcc00da5f6e" />

El resultado de ejecutar debe ser como la captura de pantalla adjuntado.

Extraemos el archivo descargado.

*unzip awscliv2.zip*

Una vez extraido, ejecutamos: 

*sudo ./aws/install*

*aws --version* | Para asegurarnos que se ha instalado y que sea la version correcta.
# Instalacion Terraform

Ahora pasamos con TerraForm, bien, el primer paso es instalar las dependencias

*sudo apt-get install -y software-properties-common wget*

Seguidamente procedemos a descargar e instalar las claves GPG de HashiCorp

*wget -O- https://apt.releases.hashicorp.com/gpg | \
    gpg --dearmor | \
    sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg*


