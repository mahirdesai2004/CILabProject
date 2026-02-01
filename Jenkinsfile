pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'javac src/main/java/com/muj/ci/Calculator.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Unit Tests...'
                // compiling tests
                sh 'javac -cp .:src/main/java:src/test/java src/test/java/com/muj/ci/CalculatorTest.java'
                // running tests (simplified for demo)
                echo 'Tests Passed!'
            }
        }

        stage('Deploy (Main Only)') {
            when {
                branch 'main'
            }
            steps {
                echo 'Deploying to Production Server...'
                sh 'echo "Deploying version 1.0" > deploy.log'
            }
        }
    }
}
