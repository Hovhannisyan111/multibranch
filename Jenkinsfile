pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Save files to be used later
                    stash name: 'buildArtifacts', includes: '**/*.jar'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Retrieve the saved files
                    unstash 'buildArtifacts'
                    echo 'Deploying artifacts'
                }
            }
        }
    }
}
