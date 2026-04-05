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

print("Add:", add(2,3))
print("Subtract:", subtract(5,2))
print("Multiply:", multiply(2,4))
print("Divide:", divide(10,2))
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
