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
                sh 'rm -rf /var/www/html/stat-web/*'
                sh 'cp -r * /var/www/html/stat-web/'
            }
        }
    }

    post {
        success {
            echo 'Deployment to Apache successful!'
        }
        failure {
            echo 'Deployment failed. Check Jenkins logs.'
        }
    }
}
