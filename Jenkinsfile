pipeline {
    agent any
    stages {
        stage ('fetch code') {
            step {
                git branch: 'main', url: 'https://github.com/mcpatral/mcpatral.git'
            }
        }
        stage ('Build') {
            steps {
                sh 'mvn install'
            }
        }
        stage ('test') {
            step {
                sh 'mvn test'
            }
        }
    }
}