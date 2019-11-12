pipeline {
    agent any
    stages {
        agent { 
                label 'SLAVE_Runner'
            }
        stage('Back-end') {
            agent {
                docker { image 'maven:3-alpine' }
            }
            
            steps {
                sh 'mvn --version'
            }
        }
        
    }
}
