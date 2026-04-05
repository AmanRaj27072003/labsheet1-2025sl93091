pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo "Cloning repository..."
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Build stage"
            }
        }

        stage('Test') {
            steps {
                sh '''
                python3 - <<EOF
from calculator import add, subtract, multiply, divide

assert add(2,3) == 5
assert subtract(5,2) == 3
assert multiply(2,4) == 8
assert divide(10,2) == 5
print("All test passed")
EOF
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy stage"
            }
        }
    }
}
