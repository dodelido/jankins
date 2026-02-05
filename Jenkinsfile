pipeline {
    agent any

    stages {
        stage('Run Robot Framework Tests') {
            steps {
                sh '''
                robot tests/Lab8.robot
                '''
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: '**/*.xml', fingerprint: true
        }
    }
}
