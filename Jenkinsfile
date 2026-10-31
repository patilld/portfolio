pipeline {
    agent any
    options {
        timeout(time: 30, unit: 'MINUTES')
        buildDiscarder(logRotator(numToKeepStr:'3', artifactNumToKeepStr:'3'))
    }
    tools {
        maven 'maven'
    }
    stages {
        stage("Code compilation") {
            steps {
                echo "Code compilation started..."
                sh 'mvn clean compile'
                echo "Code compilation completed."
            }
        }
    }

}