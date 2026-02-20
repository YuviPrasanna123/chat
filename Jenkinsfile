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
    }
}
