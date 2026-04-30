// Jenkinsfile - Pipeline declaratif
pipeline {
agent any
// Le pipeline s'execute sur n'importe quel agent disponible
stages {
stage('Build') {
steps {
echo '=== Etape 1 : Build ==='
echo 'Compilation du projet en cours...'
sh 'cat README.md'
}
}
stage('Test') {
steps {
echo '=== Etape 2 : Test ==='
echo 'Execution des tests...'
sh 'node test.js'
}
}
stage('Deploy') {
steps {
echo '=== Etape 3 : Deploy ==='
echo 'Deploiement en production...'
echo 'Application deployee avec succes !'
}
}
}
post {
always {
echo 'Pipeline termine !'
}
success {
echo 'SUCCES : toutes les etapes sont passees'
}
failure {
echo 'ECHEC : une etape a echoue'
}
}
}
