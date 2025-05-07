pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build'
            }
        }

        stage('Test') {
            steps {
                echo 'Test'
            }
        }

        stage('Integration Tests') {
            steps {
                echo 'Running integration tests'
            }
        }

        stage('Maven Version Check') {
            agent {
                docker {
                    image 'maven:3.9.9'
                    label ''  // Optional: define a label if needed
                    args '-v' // Optional: pass any docker args
                }
            }
            steps {
                sh 'mvn --version'
            }
        }
    }
}
