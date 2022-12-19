 # Install Mysql in Ubuntu
 Ubuntu Terminal
 
              $ sudo apt update
              $ sudo apt install mysql-server
              # configure mysql 
              $ sudo mysql_secure_installation
  # Create mysql  user and access to host           
Ubuntu Terminal
               # root login
               $ mysql -u root -p
  # Create user with password
  After mysql login- Terminal
  (ubuntu- replace with user user name)
  
               $ CREATE USER 'ubuntu'@'%' IDENTIFIED BY 'Sajan_aws1';
               $ GRANT ALL PRIVILEGES ON *.* TO 'ubuntu'@'%';
               $ CREATE USER 'ubuntu'@'localhost' IDENTIFIED BY 'Sajan_aws1';
               $ GRANT ALL PRIVILEGES ON *.* TO 'ubuntu'@'localhost';
               $ CREATE USER 'ubuntu'@'127.0.0.1' IDENTIFIED BY 'Sajan_aws1';
               $ GRANT ALL PRIVILEGES ON *.* TO 'ubuntu'@'127.0.0.1';
               $ FLUSH PRIVILEGES;
               
  # python connector for mysql
  
  [Mysql Doc](https://dev.mysql.com/downloads/connector/python/)
  Ubuntu Terminal
  
            pip install mysql-connector-python
            
   Python Script
   first create a database and table on mysql, then try to access the 
   file -mysqlpycode.py (any name)
   sajan- replace with username
   
          import mysql.connector
          from mysql.connector import errorcode

          try:
            cnx = mysql.connector.connect(user='sajan', 
                                          password='password',
                                          host='127.0.0.1',
                                          database='employees')
          except mysql.connector.Error as err:
            if err.errno == errorcode.ER_ACCESS_DENIED_ERROR:
              print("Something is wrong with your user name or password")
            elif err.errno == errorcode.ER_BAD_DB_ERROR:
              print("Database does not exist")
            else:
              print(err)
          else:
            cnx.close()
