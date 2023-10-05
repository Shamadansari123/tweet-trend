pipeline {
    agent {
        node {
            label 'maven-slave-node'
        }
    }

environment {
    PATH = "/opt/maven/bin/:$PATH"
}

    stages {
        stage('build code') {
            steps {
                 sh 'mvn clean deploy'
            }
        }
    }
}
