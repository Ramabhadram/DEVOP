pipeline {
    
agent { label 'ubuntu' }
    
     
  
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
                echo "vrbs"
            }
        }
           
        
        stage('Deploy') {
            steps {
                sh 'sudo apt update -y'
                sh 'sudo apt install tomcat8 -y'
                sh 'sudo apt install tomcat8-admin -y'
                sh 'sudo apt install tomcat8-user -y'
                sh 'sudo cp /home/grants.war /var/lib/tomcat8/webapps/'
                sh 'sudo cp /home/tomcat-users.xml /etc/tomcat8/'
                sh 'sudo service tomcat8 restart'
            }
        }
    }
}
