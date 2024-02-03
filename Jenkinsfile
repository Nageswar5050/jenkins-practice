pipeline {
    agent any
    stages {
        stage('Greet') {
            steps {
                echo 'Hello World'
            }
        }
    }
    post {
        always {
            echo 'I will always say Hello again!'
        }
    }
}

pipeline {
    agent any
    stages {
        stage ('Wish') {
            steps{
                echo "Hi"
            }
        
        }
    }
    post {
        always {
            echo "I also will always run"
        }
    }
}