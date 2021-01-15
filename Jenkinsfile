pipeline{
    agent any
    stages{
        stage("Build BACKeND"){
            steps{
               bat 'mvn clean package -DskipTests=true'
            }            
        }
        
    }
}