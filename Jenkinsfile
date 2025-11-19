pipeline {
    stages {
        stage ('DeploytoDev') {
            steps {
                echo "**** Deploying to dev environment ****"
            }
        }
        stage ('DeploytoTest') {
            steps {
                echo "**** Deploying to test environment ****"
            }
        }
        stage ('DeploytoStage') {
            steps {
                echo "**** Deploying to stage environment ****"
            }
        }
        stage ('DeploytoProd') {
            steps {
                timeout(time: 10, unit: 'SECONDS') {
                    input message: 'Approve deployment to production?', ok: 'Deploy'
                }
                echo "**** Deploying to prod environment ****"
            }
        }
    }
}
