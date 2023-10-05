pipeline {
    agent {
        node {
            label 'maven-slave-node'
        }
    }

    stages {
        stage('build code') {
            steps {
                 sh 'mvn clean deploy'
            }
        }
    }
}
