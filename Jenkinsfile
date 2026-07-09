pipeline {
    agent any
    
    stages{
        stage ("checkout code"){
            steps{
                bat "dir"
                git branch: 'main', url: 'https://github.com/burnoz/course3-jenkins-gs-spring-petclinic'
                bat "dir"
            }
        }
        
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