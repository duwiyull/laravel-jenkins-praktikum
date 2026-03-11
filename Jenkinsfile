pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                checkout scm
            }
        }

        stage('Test Jenkins') {
            steps {
                sh 'echo "Jenkins Pipeline berhasil dijalankan"'
            }
        }

        stage('Deploy') {
            steps {
                sshagent(['ssh-prod']) {
                    sh 'echo "Deploy menggunakan SSH berhasil"'
                }
            }
        }

    }
}