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
 sh 'docker build -t php-webapp-demo .'
 echo 'Running Docker container...'
 // Stop and remove any existing container with the same name
 sh 'docker rm -f php-webapp-demo || true'
 sh 'docker run -d --name php-webapp-demo -p 8080:80 php-webapp-demo'
 }
 }
 }
 stage('Test') {
 steps {
 echo 'Jenkins successfully pulled code from GitHub!'
 }
 }
 }
}
