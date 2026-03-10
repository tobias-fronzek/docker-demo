pipeline {
    agent {
        node {
            label 'docker-agent'
        }
    }
    tools {
        maven 'Maven3'
        jdk 'JDK21'
    }
    stages {
        stage('Build') {
            steps {
                withMaven {
                    sh 'mvn clean package -DskipTests'
                }
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