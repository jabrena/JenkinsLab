pipeline {
    agent {
            docker { image 'openjdk:8-jre-alpine' }
    }
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
