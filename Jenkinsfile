pipeline {
    agent any 
    stages {
        stage('Execution-SQL_server') { 
            steps {
               
             //sh label: '', script: 'sqlcmd -S 192.168.223.128 -U sa -P Laboratorio1 -d Laboratorio -d Laboratorio -i sql-query.sql -o file-output.txt'
             sh label: '', script: 'sqlcmd -S 192.168.223.128 -U sa -P Laboratorio1 -d Laboratorio '
             sh label: '', script: '''INSERT INTO dbo.test ([Codigo],[Nombre]) VALUES ( 3, N\'FabioGil\') GO'''          
              }
            }
        }
    }
