pipeline {
    agent any
    stages {
        stage('Install Puppet Agent') {
            steps {
                echo 'Simulating Puppet agent installation...'
            }
        }
        stage('Install Docker with Ansible') {
            steps {
                echo 'Simulating Docker installation with Ansible...'
            }
        }
        stage('Build and Deploy PHP Docker Container') {
            steps {
                script {
                    echo 'Building Docker image...'
                    sh '/usr/local/bin/docker build -t php-webapp-demo .'
                    echo 'Removing any existing container...'
                    sh '/usr/local/bin/docker rm -f php-webapp-demo || true'
                    echo 'Running Docker container...'
                    sh '/usr/local/bin/docker run -d --name php-webapp-demo -p 8080:80 php-webapp-demo'
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Jenkins successfully pulled code from GitHub!'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Simulating deployment to production...'
                // Add real deployment steps here if needed
            }
        }
    }
    post {
        failure {
            echo 'Build failed! Cleaning up Docker container if it exists...'
            sh '/usr/local/bin/docker rm -f php-webapp-demo || true'
        }
    }
}
