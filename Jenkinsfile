pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                timeout(time: 30, unit: 'MINUTES') {
                    echo 'Building...'
					sleep(time: 35, unit: "SECONDS")
                    // Simulate a long-running task
                }
            }
        }
    }
}

