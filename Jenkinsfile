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
 // In a real setup, you might use:
 // sh 'ansible-playbook -i inventory install_docker.yml'
 }
 }
 stage('Test') {
 steps {
 echo 'Jenkins successfully pulled code from GitHub!'
 }
 }
 }
}
