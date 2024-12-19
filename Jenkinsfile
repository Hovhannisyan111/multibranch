pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building project...'
                // Add your build steps here, e.g., compile code, run tests, etc.
            }
        }
        
        stage('Approval') {
            steps {
                script {
                    // Pausing the pipeline and asking for manual approval
                    def userInput = input(
                        id: 'UserInput', message: 'Approve deployment?', parameters: [
                            string(defaultValue: 'Yes', description: 'Do you want to deploy?', name: 'Deploy')
                        ]
                    )
                    
                    // Handle the input value, if needed
                    echo "User input: ${userInput}"
                }
            }
        }

        stage('Deploy') {
            when {
                expression {
                    // Only run deploy if user input is 'Yes'
                    return params.Deploy == 'Yes'
                }
            }
            steps {
                echo 'Deploying project...'
                // Add your deployment steps here
            }
        }
    }
}
