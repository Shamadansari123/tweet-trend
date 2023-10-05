pipeline {
    agent {
        node {
            label 'maven-slave-node'
        }
    }

    stages {
        stage('clone code') {
            steps {
                git branch: 'main', url: 'https://github.com/Shamadansari123/tweet-trend.git'
            }
        }
    }
}

