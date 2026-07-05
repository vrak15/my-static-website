pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Cloning GitHub Repository'
                checkout scm
            }
        }

        stage('Deploy Website') {
            steps {
                sh '''
                echo "Deploying Website..."

                cp index.html style.css script.js /var/www/html/

                echo "Deployment Completed"
                '''
            }
        }

    }

    post {

        success {
            echo 'Website deployed successfully'
        }

        failure {
            echo 'Deployment Failed'
        }

    }

}
