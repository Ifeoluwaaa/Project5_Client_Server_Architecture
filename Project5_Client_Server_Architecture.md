#### IMPLEMENTING A CLIENT SERVER ARCHITECTURE USING MySQL DATABASE MANAGEMENT SYSTEM (DBMS)
>  Create and configure two linux-based virtual servers (ubuntu)

![servers](./images/Capture.PNG)

> On mysql server linux server install MySQL server software

    sudo apt install mysql-server
![server_install](./images/Sudo_apt_update.PNG)
![server_install](./images/sudo_install_myswl_server.PNG)

> After installing log into mysql

![server_install](./images/install_and_log_into_sql.PNG)

> Set password

    sudo mysql -p

![password](./images/Confirm_Password.PNG)

> Create a TCP port 3306 for mysql server virtual server

![3306](./images/3306.PNG)

> On mysql client linux server install MySQL client software

    sudo apt install mysql-client-core-8.0

![mysql_client](./images/Second_server_sudo_apt.PNG)

> IP access should only be given to the local IP address of mysql client virtual server
> Configure MySQL server to allow connections from remote hosts

    sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf

> Change bind-address to 0.0.0.0

![bind](./images/correct_connecting_the_servers_bind.PNG)
> Close and save the file, the log out of zoom

![PIC](./images/After_install_exit.PNG)

> Create a user with a home directory and give it password

     CREATE USER 'ifeoluwa'@'local-Ip-address' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';

![password](./images/set_code_for_password.PNG)

> Create a database and grant the user all permissions and access to the database

    GRANT ALL PRIVILEGES ON *.* TO 'ifeoluwa'@'local-ip-address' WITH GRANT OPTION;

    FLUSH PRIVILEGES;
![pic](./images/Create_database.PNG)

> Test the connection of the servers using private ip address of the server mysql along side the username and password on client server.

![pic](./images/client_sserver_test.PNG)
> Sucessfully connected Mysql server to Mysql client virtual servers

