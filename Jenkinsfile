properties([
    parameters([
        string(name: 'Database'       , defaultValue: 'Laboratorio'),
        string(name: 'Host'           , defaultValue: '192.168.233.128'),
        string(name: 'User'           , defaultValue: 'sa'),
        string(name: 'Pass'           , defaultValue: 'Laboratorio1'),              
        //string(name: 'SqlPackagePath' , defaultValue: 'C:\\SSDTTools\\Microsoft.Data.Tools.Msbuild\\lib\\net46\\sqlpackage.exe')              
  ])
])

pipeline {
    agent any 
    stages {
        stage('Conection') { 
            steps {
                def ConnString = "server=${params.Host};user=${params.User};pass=${params.Pass};database=${params.Database}"
              
               // pwd
                //mssql-cli i-sql-query -o file-output.txt
                //mssql-cli -S (192.168.223.128) -U sa -P Laboratorio1 -d Laboratorio1 -i sql-query.sql -o file-output.txt
                
                
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
