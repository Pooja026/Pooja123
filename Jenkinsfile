pipeline {
    agent any

    stages {
       
        stage('git repo & clean') {
            steps {
               // bat "rmdir  /s /q  Pooja123"
                bat "git clone https://github.com/Pooja026/Pooja123.git"
                bat "mvn clean -f Pooja123"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f Pooja123"
            }
        }
        stage('Test') {
            steps {
                bat "mvn test -f Pooja123"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f Pooja123"
            }
        }
    }
}
