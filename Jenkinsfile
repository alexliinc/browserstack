pipeline {
    agent any
    tools {
        maven 'Maven 3.3.9'
        jdk 'jdk8'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                    echo "inital"
                '''
            }
        }
        stage('Build') {
            steps {
               sh 'mvn test -P parallel'
               echo "build"
            }
        }
    }
}