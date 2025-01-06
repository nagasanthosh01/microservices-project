pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t santhu156/service:v1 .'
            }
        }
        stage("Push") {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'docker-cred') {
                        sh 'docker push santhu156/service:v1 '
                    }
                }
            }
        }
    }
}
