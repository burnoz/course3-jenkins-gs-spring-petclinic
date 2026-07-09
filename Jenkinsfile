pipeline {
    agent any
    
    stages{
        stage ("build"){
            steps{
                bat ".\\mvnw.cmd package"
            }
        }
        
        stage ("capture"){
            steps{
                archiveArtifacts artifacts: '**/target/*.jar'
            }
        } 
    }
    
    post{
        always{
            bat "echo ble"
        }
    }
}