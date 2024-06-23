pipeline {
    agent any
    stages {
        stage('Install dependencies'){
            steps {
                sh "npm install" 
            }
        }
        stage('Start App') {
            steps {
                sh "npm run start &"
            }
        }
        stage('Run Tests') {
            steps {
                sh "npm run test"
            }
        }
    }
    post {
        always {
            echo 'Cleaning workspace'
            cleanWs()
        }
    }
}