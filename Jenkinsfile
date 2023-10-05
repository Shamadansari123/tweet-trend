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
    
    
        stage ('test'){
               steps {
                 sh 'mvn surefire-report:report'
               }
               
        }
        stage('SonarQube analysis') {
            environment {
                scannerHome = tool 'shamad-sonar-scanner'}
            steps {
                withSonarQubeEnv('shamad-sonar-server') { // If you have configured more than one global server connection, you can specify its name
        sh "${scannerHome}/bin/sonar-scanner"
        }
            }
    }
}
}

