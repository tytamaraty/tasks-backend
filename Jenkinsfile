pipeline{
    agent any
    stages{
        stage("Build BACKeND"){
            steps{
               bat 'mvn clean package -DskipTests=true'
            }            
        }
         stage("Units_Tests"){
            steps{
               bat 'mvn tests'
            }            
        }
    }
}