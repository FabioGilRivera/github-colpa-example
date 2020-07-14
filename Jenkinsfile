pipeline {
    agent any 
    stages {
        stage('Conection') { 
            steps {
                //def ConnString = "server=${params.Host};user=${params.User};pass=${params.Pass};database=${params.Database}"
           // sh sqlcmd -S 192.168.223.128 -U sa -P Laboratorio1 -d Laboratorio -i sql-query.sql -o file-output.txt
               // pwd
                //mssql-cli i-sql-query -o file-output.txt
                //mssql-cli -S (192.168.223.128) -U sa -P Laboratorio1 -d Laboratorio1 -i sql-query.sql -o file-output.txt
            dir('sql-files'){
                        sh '''export PATH=/bin/bash:$PATH
                    	      cat sql-query.sql
                              mssql-cli -S 192.168.223.128 -U sa -P Laboratorio1 -d Laboratorio -i sql-query.sql -o file-output.txt
                        '''    
                
                echo"welcome" 
            }
            }
        }
        stage('Execution -Package') { 
            steps {
               echo"Ejecucion SQL" 
            }
        }
        stage('Execution -Deploy') { 
            steps {
                echo "Ejecucion satisfactoria" 
            }
        }
    }
}
