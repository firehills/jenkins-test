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
                sleep time:5 unit: SECONDS
                echo 'Done'
            }
        }
        stage('Debug') {
            steps {
                echo 'Debug env vars for jenkins-test....'
                sh 'sleep 5'
                echo 'BUILD_ID=${env.BUILD_ID}'
                echo 'BUILD_DISPLAY_NAME=${env.BUILD_DISPLAY_NAME}'
                echo 'JOB_NAME=${env.JOB_NAME}'
                echo 'BUILD_URL=${env.BUILD_URL}'
                echo 'durationString=${currentBuild.durationString}'
                echo 'TAG_NAME=${env.TAG_NAME}'
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
