pipeline {
    agent any 
    stages {
        stage('Execution-SQL_server') { 
            steps {
             echo"Ejecucion SQL - Insert"  
             sh label: '', script: 'sqlcmd -S 192.168.223.128 -U sa -P Laboratorio1 -d Laboratorio -d Laboratorio -i sql-query.sql -o file-output.txt'
             }
            }
        }
    }
