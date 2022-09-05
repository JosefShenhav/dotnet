pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    dotnetBuild()
                }
                 
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
