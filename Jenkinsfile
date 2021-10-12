pipeline {
    agent any
    parameters {
        choice(name: 'VERSION', choices:['1.1.0', '1.2.0', '1.3.0'], description:'Enter version number')
        booleanParam(name: 'executeTests', defaultValue: true, descriptio:'')
    }

    stages {
        stage('Hello') {
            when{
                expression {
                    params.executeTests 
                }
            }
                
            steps {
                echo 'Hello World'
                git branch: 'main', credentialsId: 'GitHub', url: 'https://github.com/harshavn/testrepo'
            }
        }
        stage('Build') {
            steps {
                echo 'Building'
                echo "Build number $BUILD_NUMBER"
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
