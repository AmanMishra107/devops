pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out repo'
                git 'https://github.com/AmanMishra107/devops.git'
            }
        }

        stage('Publish') {
            steps {
                publishHTML([
                    allowMissing:true,
                    alwaysLinkToLastBuild:false,
                    keepAll:false,
                    reportDir:'.',
                    reportFiles:'Hello.html',
                    reportName:'My HTML Pipe Page'
                ])
            }
        }
    }
}
