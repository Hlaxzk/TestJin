pipeline {
    agent any
    node {
        stage('Update pom') {
            steps {
                sh 'echo upd pom'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Deploy To Maven') {
            steps {
                sh 'echo deploy'
            }
        }
        stage('ArchiveArtifacts') {
            steps {
                sh 'archiveArtifacts artifacts: TestJin.2.0.0-SNAPSHOT, fingerprint: true, onlyIfSuccessful: true'
            }
        }
        stage('Build DockerImage') {
            steps {
                sh 'echo build docker image'
            }
        }
    }
}