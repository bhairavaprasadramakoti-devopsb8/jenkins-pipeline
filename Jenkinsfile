pipeline {
    agent {
        label 'java-slave'
    }
    tools {
        maven 'MAVEN_3.9.8' // specify the same Maven installation name configured in Jenkins
    }
    stages {
        stage ('Maven') {
            steps {
                echo "hello, this is maven section"
                sh "mvn --version"
                }
            }
        }
}
