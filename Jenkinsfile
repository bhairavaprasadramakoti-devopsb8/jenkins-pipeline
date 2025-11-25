pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage ('Build') {
            steps {
                echo "Building the application"
                }
                
        }
    }
    post {
        // this will only run, when the current pipeline or stage is having a success stage
        success {
            echo "**** Post ============> Success is triggered"
            // mail logic
        }
        // Runs only when the pipeline or stage is having a failure status
        failure {
            echo "**** Post =============> Failure is triggered"
            // mail logic
        }
        // this will run irrespective of the failed or success, everytime it should run
        always {
            // mail logic
            echo "**** Post ============> Success is triggered"
        }
    }
}
