pipeline {
    agent any
    stages {
        stage('Chekout') {
            steps {
                git branch: 'main', credentialsId: 'jenkins', url: 'git@github.com:Jalolboy/Jenkins-private.git'
            }
        }
        stage('Stage2') {
            steps {
                sh '''ls /var/lib/jenkins
                    echo "testing pipeline"'''
            }
        }
        stage('Stage3') {
            steps {
                echo 'Build number is : ${env.BUILD_NUMBER}'
            }
        }

    }
    post {
        always {
            cleanWs()
        }
    }
}
