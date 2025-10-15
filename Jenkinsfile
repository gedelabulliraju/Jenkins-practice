pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        timeout(time: 10, unit: 'MINUTES') // Timeout after 10 minutes
        disableConcurrentBuilds() // Prevent concurrent builds
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'echo "Building the project..."'
                //sh 'sleep 3' // Simulate a build step
            }
        }
        stage('Test') {
            steps {
                echo 'Testing.........'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...........'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
            deleteDir() // Clean up workspace
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the pipeline has changed'
        }
    }
}