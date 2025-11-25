pipeline {
    agent {
        label 'java-slave'
    }
    stages {
        stage ('Build') {
            steps {
                echo "**** Building maven application ****"
            }
        }
        stage ('CodeAnalysis') {
            steps {
                echo "**** Running Sonar scan ****"
            }
        }
        stage ('DockerBuildnPush') {
            steps {
                echo "**** Build and push docker images ****"
            }
        }
        stage ('DeployToDev') {
            steps {
                echo "***** Deploying to dev env *****"
            }
        }
        stage ('DeployToTest') {
            steps {
                echo "***** Deploying to Test env *****"
            }
        }
        stage ('DeployToStage') {
            steps {
                echo "***** Deploying to Stage env *****"
            }
        }
        stage ('DeployToProd') {
            options {
                timeout (time: 300, unit: 'SECONDS')
            }
            input {
                message "Doing Prod Deployment ?????"
                ok 'yes'
                submitter 'bhairava,RaghuSRE'
            }
            steps {
                echo "***** Deploying to Prod env *****"
            }
        }
    }
}
