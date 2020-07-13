pipeline {
    agent any 
    stages {
        stage('Conection') { 
            steps {
                pwd
               // mssql-cli -S  '192.168.223.128' -U administrador -P Laboratorio1 -d TutorialDB 
                
                mssql-cli -S (192.168.223.128) -U sa -P Laboratorio1 -d Laboratorio1 -i sql-query.sql -o file-output.txt
                
                
                echo"welcome" 
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
