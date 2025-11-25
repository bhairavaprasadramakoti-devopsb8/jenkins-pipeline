pipeline {
    agent {
        label 'java-slave'
    }
    parameters {
        string (
            name: 'PERSON',
            defaultValue: 'Siva',
            description: 'Whats your name???'
        )
        choice (
            name: 'DEPLOYTOENV',
            choices: ['dev', 'test', 'stage'],
            description: 'Which env should we deploy'
        )
        booleanParam(
            name: 'TOOGLE',
            defaultValue: true,
            description: 'Is this release approved by SRE ????'
        )
        text (
            name: 'RELEASEDETAILS',
            defaultValue: '',
            description: 'Enter some details about whats deploying today'
        )
    }
    stages {
        stage ('ParametersStage') {
            steps {
                echo "Hello, ${params.PERSON}"
                echo "Release Notes: ${params.RELEASEDETAILS}"
                echo "Is this release approved by SRE ? ${params.TOOGLE}"
                echo "Selected ENV to deploy is: ${params.DEPLOYTOENV}"
            }
        }
    }
}
