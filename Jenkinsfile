


pipeline {
   agent any
   parameters {
        string(name: 'ENV', defaultValue: 'DEV', description: 'Where you want to do the deployment?')
         string(name: 'ENV', defaultValue: 'SIT', description: 'Where you want to do the deployment?')
         string(name: 'ENV', defaultValue: 'PROD', description: 'Where you want to do the deployment?')
    }
    stages {
       
        stage('Build') {
           
           agent { 
               label 'dev'
            }
            steps {
                echo 'Building..'
                 sh 'mvn package'
            }
        }
       
   
        stage('Deploy') {
           agent { 
               label 'dev'
            }
            
            steps {
                
                sh 'sudo apt update -y'
                sh 'sudo apt install tomcat8 -y'
                sh 'sudo apt install tomcat8-admin -y'
                sh 'sudo apt install tomcat8-user -y'
                sh 'sudo cp /home/ubuntu/workspace/Deployment/target/grants.war /var/lib/tomcat8/webapps/'
                sh 'sudo cp /home/ubuntu/workspace/Deployment/tomcat-users.xml /etc/tomcat8/'
                sh 'sudo service tomcat8 restart'
            }


     agent { 
               label 'sit'
            }
            steps {
                echo 'Building..'
                 sh 'mvn package'
            }
        }
       
   
        stage('Deploy') {
           agent { 
               label 'sit'
            }
            
            steps {
                
                sh 'sudo apt update -y'
                sh 'sudo apt install tomcat8 -y'
                sh 'sudo apt install tomcat8-admin -y'
                sh 'sudo apt install tomcat8-user -y'
                sh 'sudo cp /home/ubuntu/workspace/Deployment/target/grants.war /var/lib/tomcat8/webapps/'
                sh 'sudo cp /home/ubuntu/workspace/Deployment/tomcat-users.xml /etc/tomcat8/'
                sh 'sudo service tomcat8 restart'
            }




    agent { 
               label 'prod'
            }
            steps {
                echo 'Building..'
                 sh 'mvn package'
            }
        }
       
   
        stage('Deploy') {
           agent { 
               label 'prod'
            }
            
            steps {
                
                sh 'sudo apt update -y'
                sh 'sudo apt install tomcat8 -y'
                sh 'sudo apt install tomcat8-admin -y'
                sh 'sudo apt install tomcat8-user -y'
                sh 'sudo cp /home/ubuntu/workspace/Deployment/target/grants.war /var/lib/tomcat8/webapps/'
                sh 'sudo cp /home/ubuntu/workspace/Deployment/tomcat-users.xml /etc/tomcat8/'
                sh 'sudo service tomcat8 restart'
            }




        }
    }
}


