pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building"'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing"'
            }
        }
        stage('Publish') {
            steps {
                sh 'echo "Publishing"'
            }
            post {
                success {
                    sh 'echo "Deploying to EB"'
                    sh 'sudo chmod 775 ./deployme.sh'
                    sh './deployme.sh'
                }
            }
        }
    }
}
