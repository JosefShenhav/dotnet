pipeline {
    agent any

    stages {
        stage('Build') {
            steps {      
                script {
                    def scannerHome = tool 'SonarQube'
                    withSonarQubeEnv() {
                      sh "dotnet ${scannerHome}/SonarScanner.MSBuild.dll begin /k:\"lord\""
                      sh "dotnet build"
                      sh "dotnet ${scannerHome}/SonarScanner.MSBuild.dll end"
                    }
                }
            }
        }
    }
}
