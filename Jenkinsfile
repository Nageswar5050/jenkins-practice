pipeline {
    agent any
    environment {
        MY_NAME = 'JAIBALAYYA'
    }
    stages {
        stage ('Build') {
            steps {
                echo "I am Nageswar, and this is from building phase"
            }
        }

        stage ('Test') {
            steps {
                echo "this is from testing phase"
                sh """
                env
                """
            }
        }

        stage ('Deploy') {
            steps {
                echo "this is from deploying phase"
            }
        }
    }

    post {
        always {
            echo "I will always run"
        }
    }
}