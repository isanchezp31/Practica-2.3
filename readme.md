# Practica 2.3
#### Instalar clientes para tres SGBD
1. Clientes para Oracle Database en MINT.
  - **lo primero que vamos a descargar es un JDK para la version que tenemos instalada para SQL Developer**
  - vamos a instalar JDK con "sudo apt install default-jdk unzip"
  - Despues vamos a descargar el zip de SQL para linux con el siguiente comando "sudo unzip Nombre_del_archivo.zip -d /opt/" y despues ejecutamos "/opt/sqldeveloper/sqldeveloper.sh"
  - Una vez ya iniciado vamos a crear una conexion con el usuario orauser "sudo tee /usr/share/applications/sqldeveloper.desktop > /dev/null <<'EOT | [Desktop Entry] | Version=1.0 | Name= SQL Developer | Comment=Entorno de desarrollo SQL | Exec=/opt/sqldeveloper/sqldeveloper.sh | Icon=/opt/sqldeveloper/icon.png | Terminal=false | Type=application | categories=Development;Database; | Keywords=database;db;sql;query;administration; | EOT"
  - **Ahora vamos a instalar VS Code y la extension de Developer**
  - para ello entramos a la carpeta de descargas con "cd Descargas" y lo instalamos con "sudo apt install ./Nombre_del_archivo.deb"
  - e instalamos la extension de oracle SQL Developer en el apartado de extensiones de VS Code
