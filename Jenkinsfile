pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo '=== Etape 1 : Build ==='
                echo 'Compilation du projet en cours...'
                bat 'type README.md'
            }
        }

        stage('Test') {
            steps {
                echo '=== Etape 2 : Test ==='
                echo 'Execution des tests...'
                bat 'node test.js'
            }
        }

        stage('Deploy') {
            steps {
                echo '=== Etape 3 : Deploy ==='
                echo 'Deploiement en cours...'

                // créer le dossier de déploiement
                bat 'if not exist C:\\deploy\\mon-app mkdir C:\\deploy\\mon-app'

                // copier les fichiers
                bat 'xcopy /E /I /Y * C:\\deploy\\mon-app'

                echo 'Application deployee dans C:\\deploy\\mon-app'
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
