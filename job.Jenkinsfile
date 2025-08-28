pipeline {
    agent any  // Use any available agent

    stages {
        stage('Checkout') {
            steps {
                // Clone the code from your Git repository
                git url: 'https://github.com/Chetan0918/Dev-ops-lab', branch: 'main'  // Replace with your repository URL and branch
            }
        }

        stage('Set Up Python Environment') {
            steps {
                script {
                    // Check if Python is installed, or install it
                    sh 'python3 --version'  // Or use `python --version` if needed
                    // Optionally set up a virtual environment if you have dependencies
                    // sh 'python3 -m venv venv'  // Uncomment if using a virtual environment
                    // sh 'source venv/bin/activate'  // Uncomment if using a virtual environment
                }
            }
        }

        stage('Run Python Script') {
            steps {
                script {
                    // Run the Python Hello World script
                    sh 'python3 hello_world.py'  // This will execute your Python script
                }
            }
        }
    }

    post {
        always {
            // Clean up or any final steps if needed
            echo 'Build finished.'
        }
    }
}
