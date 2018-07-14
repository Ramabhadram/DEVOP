pipeline {
    agent any
    stages {
        
        stage('Build') {
            steps {
                echo 'Building..'
                 sh 'mvn package'
            }
        }
        stage('Decision') {
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "admin"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
            }
            steps {
                echo 'vrbs'
            }
        }
           
        
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
