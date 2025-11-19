pipeline {

    agent { // where should this job be running on ?
        label 'java-slave'
    }
    stages {
        stage ('hostname') {
            steps {
                sh 'hostname -i'
            }
        }
    }
}
