# Practica 2.3
#### Instalar clientes para tres SGBD
1. Clientes para Oracle Database en MINT.
  - **1.1 lo primero que vamos a descargar es un JDK para la version que tenemos instalada para SQL Developer**
  - vamos a instalar JDK con "sudo apt install default-jdk unzip"
  - Despues vamos a descargar el zip de SQL para linux con el siguiente comando "sudo unzip Nombre_del_archivo.zip -d /opt/" y despues ejecutamos "/opt/sqldeveloper/sqldeveloper.sh"
  - Una vez ya iniciado vamos a crear una conexion con el usuario orauser "sudo tee /usr/share/applications/sqldeveloper.desktop > /dev/null <<'EOT | [Desktop Entry] | Version=1.0 | Name= SQL Developer | Comment=Entorno de desarrollo SQL | Exec=/opt/sqldeveloper/sqldeveloper.sh | Icon=/opt/sqldeveloper/icon.png | Terminal=false | Type=application | categories=Development;Database; | Keywords=database;db;sql;query;administration; | EOT"
  - **1.2 Ahora vamos a instalar VS Code y la extension de Developer**
  - para ello entramos a la carpeta de descargas con "cd Descargas" y lo instalamos con "sudo apt install ./Nombre_del_archivo.deb"
  - e instalamos la extension de oracle SQL Developer en el apartado de extensiones de VS Code
  - **1.3 Cliente terminal SQL Plus**
  - para instalarlo nos vamos a la pagina de oracle e instalamos el zip
  - una vez instalados los dos zip creamos una carpeta para descomprimir los dos ahi "mkdir /oracle-client" "unzip instantclient-basic-linux.x64-23.26.4.0.0.zip -d ~/oracle-client | unzip instantclient-sqlplus-linux.x64-23.26.4.0.0.zip -d ~/oracle-client"
  - Exportamos las variables de entorno "export LD_LIBRARY_PATH="$HOME/oracle-client/instantclient_XX_X:$LD_LIBRARY_PATH"" | "export PATH="$HOME/oracle-client/instantclient_XX_X:$PATH""
  -  creamos una conexion con orauser "sqlplus orauser@//localhost:1521/FREEPDB1"
  -  **1.4 Cliete de terminal SQLcl**
  -  Ahora vamos a instalar sqlcl para ello ejecutamos el siguiente comando "sud apt install default-jdk unzip" y vemos la versio de java instalada "java --versionjava"
  -  Y descargamos SQLcl desde la pagina de oracle, en la terminal nos metemos en descargas y descomprimimos el zip que hemos descargado "unzip nombre_del_archivo.zip -d ~/sqlcl"
  -  para poder ejecutar sql desde cualquier terminal añadimos esto "export PATH="$HOME/sqlcl/sqlcl/bin:$PATH""
2. Clientes para PostgreSQL
  - **2.1 Cliente de terminal psql**
  - vamos a instalar el cliente y a conectarnos para instalar "sudo apt install postgresql-client"  para ver la version "psql --version" para conectarnos "psql -h localhost -U pguser -d dbpg -W"
  - **2.2 Cliente grafico pgAdmin 4**
  - Vamos a configurar el repositorio oficial de pgAdmin 4 e instalamos la version de escritorio "sudo apt install curl gnupg lsb-release" | "curl -fsS https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo gpg --dearmor -o /etc/apt/keyrings/packages-pgadmin-org.gpg" | "udo sh -c 'echo "deb [signed-by=/etc/apt/keyrings/packages-pgadmin-org.gpg] https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list'" | "sudo apt update" | "sudo apt install pgadmin4-desktop"
  - Una vez todo instalado nos metemos en pgadmin 4 e iniciamos la conexion por entorno grafico
3. Clientes para MariaDB
  - **3.1 Cliente de terminal: mariadb**
  - Vamos a instalar el cliente de Mariadb "sudo apt update" | "sudo apt install mariadb-client" | "mariadb --version" | "mariadb -h localhost -u muser -p dbm"
  - 
