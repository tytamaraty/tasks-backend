pipeline{
    agent any
    stages{
        stage("Build_BackEnd"){
            steps{
               bat 'mvn clean package -DskipTests=true'
            }            
        }
         stage("Units_Tests"){
            steps{
               bat 'mvn test'
            }            
        }
        stage("Sonar_analysis"){
            environment {
                scannerHome = 'SONAR_SCANNER'
            }
            steps{
                bat "${scannerHome}/bin/sonar-scanner -e -Dsonar.projectKey=DeployBack -Dsonar.host.url=http://localhost:9000 -Dsonar.login=14526640cc7b158b661d1540540967c4a2f3940b -Dsonar.java.binaries=target"
            }                                   
        }
    }
}

