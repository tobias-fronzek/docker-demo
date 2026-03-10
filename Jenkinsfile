pipeline {
    agent {
        node {
            label 'docker-agent'
            }
      }
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'maven:3.9-eclipse-temurin-21'
                }
            }

            steps {
                sh 'mvn clean package -DskipTests'
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "doing test stuff.."
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}