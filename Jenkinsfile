pipeline {
    agent any 
    stages {
        stage('Execution-SQL_server') { 
            steps {
               
           // sh sqlcmd -S 192.168.223.128 -U sa -P Laboratorio1 -d Laboratorio -i sql-query.sql -o file-output.txt
             
                //mssql-cli -S (192.168.223.128) -U sa -P Laboratorio1 -d Laboratorio1 -i sql-query.sql -o file-output.txt
            dir('sql-files'){
                        sh '''export PATH=/bin/bash:$PATH
                    	      cat sql-query.sql
                              mssql-cli -S 192.168.223.128 -U sa -P Laboratorio1 -d Laboratorio -i sql-query.sql -o file-output.txt
                        '''    
              }
            }
        }
    }
}
