pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo 'Building the app'
             }
        }
        stage('test') {
            steps {
                echo 'Testing the app'
                sh 'mvn test'
            }
          }
        stage('deploy') {
            steps {
                echo 'deploying stage'
                echo 'hi'
            }
        }
    }
}
