pipeline {
    agent {
        node {
            label "agent_1"
        }
    }
    
    stages {
        stage ("Build") {
            steps {
                echo "Building"
            }
        }
        stage ("Test") {
            steps {
                echo "Testing"
            }
        }
        stage ("Deploy") {
            steps {
                echo "Deploying"
            }
        }
    }

    post {
        always {
            echo "I will always run"
        }
        failed {
            echo "I will only run if pipeline fails"
        }
        success {
            echo "I will only run if pipeline success"
        }
    }
}