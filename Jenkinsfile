pipeline {
    agent any

    stages {
        stage('cleanws') {
            steps {
                echo 'cleanWs()'
            }
        }
        stages {
            stage('git-checkout') {
                steps {
                    git branch: 'main', url: 'https://github.com/YuviPrasanna123/chat.git'
                }
            }
        }
    }
}
