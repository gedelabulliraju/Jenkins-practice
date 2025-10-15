pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
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

post {
    always {
        echo 'This will always run after the stages finish.'
    
    }
    success {
        echo 'This will run only if the pipeline succeeds.'
    }
    failure {
        echo 'This will run only if the pipeline fails.'
    }
}