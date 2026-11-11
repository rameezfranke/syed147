pipeline {
    agent any
    tools{
        maven '3.10'
    }

    stages {
        stage('git checkout') {
            steps {
                git branch: 'main', credentialsId: '44ef3756-6c18-4644-a6a3-cdfebad07461', url: 'https://github.com/rameezfranke/syed147'
            }
        }
        stage('mvn compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('mvn test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('mvn build') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
