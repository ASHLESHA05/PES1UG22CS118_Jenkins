pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''
                echo "Compiling PES1UG22CS118.cpp"
                g++ PES1UG22CS1234.cpp -o PES1UG22CS118
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                echo "Running the compiled program"
                ./PES1UG22CS118
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment step"
            }
        }
    }

    post {
        failure {
            echo "Pipeline failed"
        }
    }
}
 
