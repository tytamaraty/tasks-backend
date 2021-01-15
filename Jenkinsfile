pipeline{
    agent any
    stages{
        stage("Build BACKEND"){
            steps{
               bat 'mvn clean package -DskipTests=true'
            }            
        }
        
    }
}