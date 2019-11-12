pipeline {
    agent {
         docker1 { image 'maven:3-alpine' }
          }
    stages {
        stage('Back-end') {
            steps {
                sh 'mvn --version'
            }
        }
        
    }
}
