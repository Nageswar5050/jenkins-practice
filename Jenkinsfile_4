pipeline {
    agent {
        node {
            label "agent_1"
        }
    }

    options {
        timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds()
    }

    environment {
        Greetins = 'Hello'
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    
    stages {
        stage ("Build") {
            steps {
                echo "Building..."
            }
        }
        stage ("Test") {
            steps {
                echo "Testing..."
            }
        }
        stage ("Deploy") {
            steps {
                echo "Deploying..."
            }
        }
        stage('pramas stage') {
            steps {
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
            }
        }
    }

    post {
        always {
            echo "I will always run"
        }
        failure {
            echo "I will only run if pipeline fails"
        }
        success {
            echo "I will only run if pipeline success"
        }
    }
}