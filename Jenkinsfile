pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                           echo "Building"
                    """
                }
            }
        }
        stage('Test') {
           stage('Build') {
            steps {
                script {
                    sh """
                           echo "Building"
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying"
            }
        }
    }
    post{
        always{
            echo 'I will always say Hello again!'
            cleanWs()
        }
        success {
            echo 'I will run if success'
        }
        failure {
            echo 'I will run if failure'
        }
    }
}