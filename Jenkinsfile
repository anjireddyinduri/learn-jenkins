pipeline {
    agent {
        label 'AGENT-1'

    }

    stages {
        stage('build') {
            steps {
                sh "echo this build new"
            }
        }

        stage('Test') {
            steps {
                sh "echo this test"
            }
        }

        stage('deploy') {
            steps {
                sh "echo this is deploy"
            }
        }
    }
}