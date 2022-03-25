pipeline {
    agent any 
    stages {
        stage('Clone Repo') { 
            steps {
                sh "rm -rf my-app"
                sh "git clone https://github.com/dinhash/my-app.git"
                sh "mvn clean -f my-app"
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test -f my-app"
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package -f my-app"
            }
        }
    }
}
