pipeline {
    agent {
        label 'AGENT-1'

    }
    options {
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    environment{
        DEPLOY_To = 'Production'
        GREETINGS = 'Good Morning'
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
        stage('print params') {
            steps {
                echo "Hello ${params.PERSON}"
                echo "Biography: ${params.BIOGRAPHY}"
                echo "Toggle: ${params.TOGGLE}"
                echo "Choice: ${params.CHOICE}"
                echo "Password: ${params.PASSWORD}"
                echo "one more time tested"
                echo "error some failure"

            }

        }
        
    }
    post {
        always {
            echo 'this code always run'
        }
        
        success {
            echo 'this will run when code success'
        }
        failure {
            echo 'this will run when code fails'
        }
    }
}