pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
            //   bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                bat "git clone https://https://github.com/Yahya-03/testpipeline.git"
                bat "mvn clean -f testpipeline"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f testpipeline"
            }
        }
        stage('test') {
            steps {
                bat "mvn test -f testpipeline"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f testpipeline"
            }
        }
    }
}
