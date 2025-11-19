pipeline {
    agent {
        label 'java-slave'
    }
    tools {
        maven 'MAVEN_3.8.9' // specify the same Maven installation name configured in Jenkins
    }
    stages {
        steps {
            echo "hello, this is maven section"
            sh "mvn --version"
        }
    }
}
