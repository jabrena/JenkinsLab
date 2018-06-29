pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                bat './mvnw clean test'
            }
        }
        stage('postActions') {
            steps {
                bat '''
                echo "hello"
                echo "world"
                '''
            }
        }
    }
    post {
        always {
            junit 'target/**/*.xml'
        }
    }
}
