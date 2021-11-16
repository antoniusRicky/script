pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
                bat "rmdir  /s /q FinalOJT"
                bat "git clone https://github.com/antoniusRicky/FinalOJT.git"
                bat "mvn clean -f Testing"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f Testing"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f Testing"
            }
        }
        
    }
}
