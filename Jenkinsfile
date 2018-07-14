pipeline {
    
agent any
    
    
  
    stages {
        
        stage('Clone sources') {
           }
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
                echo 'Deploying....'
            }
        }
    }
}
