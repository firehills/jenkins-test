pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building jenkins-test..'
                sh 'sleep 5'
                echo 'Done'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing jenkins-test..'
                sleep (time: 5, unit: "SECONDS")
                echo 'Done'
            }
        }
        stage('Debug') {
            steps {
                echo 'Debug env vars for jenkins-test....'
                sh 'sleep 5'
                echo 'BUILD_ID=${BUILD_ID}'
                echo 'BUILD_DISPLAY_NAME=${BUILD_DISPLAY_NAME}'
                echo 'JOB_NAME=${JOB_NAME}'
                echo 'BUILD_URL=${BUILD_URL}'
                echo 'durationString=${durationString}'
                echo 'TAG_NAME=${TAG_NAME}'
                echo ''
                echo 'Done'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying jenkins-test....'
                sh 'sleep 5'
                echo 'Done'
            }
        }
    }
}
