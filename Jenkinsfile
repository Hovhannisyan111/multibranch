pipeline {
    agent any
    stages {
        stage('Approval') {
            steps {
                input 'Approve to deploy?'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}

