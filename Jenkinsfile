pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo 'Building the app'
                sh 'apt-get update -y'
                sh 'apt-get install gnupg2 -y'
                sh 'gpg2 --keyserver hkp://keyserver.ubuntu.com --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB'
                sh 'curl -sSL https://get.rvm.io -o rvm.sh'
                sh 'cat rvm.sh | bash -s stable --rails'
                sh 'source ~/.rvm/scripts/rvm'
                sh 'rvm install 3.0.0'
                sh 'rvm use 3.0.0'
                sh 'bundle install'
                sh 'rails db:migrate'
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
