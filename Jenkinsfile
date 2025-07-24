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
                // Need to enable env vars Jenkins->ManageJenkins->System GlobalProperties->EnvironmentVariable 
                echo 'Debug env vars for jenkins-test....'
                echo ("BUILD_ID=${env.BUILD_ID}")
                echo ("BUILD_DISPLAY_NAME=${env.BUILD_DISPLAY_NAME}")
                echo ("JOB_NAME=${env.JOB_NAME}")
                echo ("BUILD_URL=${env.BUILD_URL}")
                echo ("durationString=${currentBuild.durationString}")
                echo ("TAG_NAME=${env.TAG_NAME}")
                echo ("")
                echo ("Done")
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
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
