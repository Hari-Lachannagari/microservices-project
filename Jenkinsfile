pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker build -t hari646/service:v1 .'
            }
        }
        stage("Docker Push") {
            steps{
                script {
                    withDockerRegistry(credentialsId: 'docker-cred') {
                        sh "dokcer push hari646/service:v1 "
}
                }
                
            }
        }
    }
}
