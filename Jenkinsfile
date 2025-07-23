groovy
pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/DikshitaJami/azure-rep.git'
            }
        }
        
        stage('Deploy to Apache') {
            steps {
                sh 'sudo cp -r * /var/www/html/stat-web/'
            }
        }
    }
}
