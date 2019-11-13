pipeline {
    agent any
    stages {
        stage('Build') { 
             steps {
                sh 'mvn clean package'
        }
        }
        stage('SonarQube analysis') { 
             steps {
                withSonarQubeEnv('sonar') {
                sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.6.0.1398:sonar'

                }
        }
        }
        }
        
    }
