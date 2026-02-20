pipeline {
    agent any

    stages {

        stage('Clean Workspace') {
            steps {
                cleanWs()
            }
        }

        stage('Git Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/YuviPrasanna123/chat.git'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('mysonar') {
                    sh '''
                    sonar-scanner \
                      -Dsonar.projectKey=MyPythonProject \
                      -Dsonar.sources=.
                    '''
                }
            }
        }
    }
}