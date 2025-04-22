pipeline {
    agent any
    stages {
        stage ("Checkout SCM") {
            steps {
                echo "This is first stage"
                sh 'exit 1'
            }
        }
       stage ("Build") {
            steps {
                echo "This is second stage"
            }
       }
    }
}