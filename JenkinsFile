pipeline {
    agent any
    options {
        timeout(time: 30, unit: 'MINUTES')
        buildDiscarder(logRotator(numToKeepStr:'3', artifactNumToKeepStr:'3'))
    }

    stages {
        stage("Code compilation") {
            steps {
                echo "Code compilation started..."
                sh './mvnw clean compile'
                echo "Code compilation completed."
            }
        }
    }

}