pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                dotnetBuild 
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
