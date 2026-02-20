pipeline {
    agent any

    stages {
        stage('cleanws') {
            steps {
                echo 'cleanWs()'
            }
        }
            stage('git-checkout') {
                steps {
                    git branch: 'main', url: 'https://github.com/YuviPrasanna123/chat.git'
                }
        }
            stage('SonarQube Analysis') { 
                steps {
                    withSonarQubeEnv('mysonar') {
                    sh '''
                          sonar-scanner \
                         -Dsonar.projectKey=MyPythonProject \
                         -Dsonar.sources=. \
                         -Dsonar.language=py
                      '''
                    }
                }
            }
    }
}

