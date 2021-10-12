pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                git branch: 'main', credentialsId: 'GitHub', url: 'https://github.com/harshavn/testrepo'
            }
        }
        stage('Build') {
            steps {
                echo 'Building'
                echo 'Build number'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
    }
}
