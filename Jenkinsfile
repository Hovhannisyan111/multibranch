pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                timeout(time: 10, unit: 'SECONDS') {
                    echo 'Building...'
					sleep(time: 15, unit: "SECONDS")
                    // Simulate a long-running task
                }
            }
        }
    }
}

