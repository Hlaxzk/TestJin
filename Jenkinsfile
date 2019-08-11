pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('archiveArtifacts') {
            steps {
                sh 'artifacts: TestJin.2.0.0-SNAPSHOT, fingerprint: true, onlyIfSuccessful: true'
            }
        }
    }
}