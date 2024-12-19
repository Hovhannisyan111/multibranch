pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                lock('my-resource') {
                    echo 'Using the locked resource'
                    // Actions that require exclusive access to a resource
                }
            }
        }
    }
}

