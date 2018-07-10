pipeline {
agent {label 'docker'}  
   
    stages {
         
        stage('Build') {
            steps {
                echo 'Building..' 
                 sh 'mvn package'
            }
        } 
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                sh 'sudo apt update -y'
                sh 'sudo apt install tomcat8 -y'
            }
        }
    }
}
 
