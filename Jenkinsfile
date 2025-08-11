pipeline {
 agent any
 stages {
 stage('Install Puppet Agent') {
 steps {
 echo 'Simulating Puppet agent installation...'
 // On a real Linux server, you might use:
 // sh 'sudo apt-get update && sudo apt-get install -y puppet-agent'
 }
 }
 stage('Test') {
 steps {
 echo 'Jenkins successfully pulled code from GitHub!'
 }
 }
 }
}
