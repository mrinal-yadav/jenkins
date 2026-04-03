pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/mrinal-yadav/jenkins.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        
        stage('Deploy Simulation') {
            steps {
                sh '''
                    echo "Deployment simulation complete: build copied to staging folder."
                '''
            }
        }
    }
}