pipeline {
    agent any
    environment {
        name = 'Test Namee'
    }
    stages {
        stage('Test') {
            steps {
                echo "Testing variable = tg"
                echo 'Testing'
            }
        }
        stage('Build') {
            environment {
                testName = 'Test Name2'
            }
            steps {
                echo "Building = builg"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
        stage('Continue') {
            input{
                message "Proceed Further"
                ok  "Yes"
            }
            steps {
                echo 'Deploying'
            }
        }
        
    }
    post{
        always{
            echo "Yes I will always run"
        }
        failure{
            echo "I have failed"
        }
        success{
            echo "Success Run Check"
        }
        aborted{
            echo "aborting here...."
        }
    }
}
