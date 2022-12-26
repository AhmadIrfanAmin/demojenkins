pipeline {
    agent any
    environment {
        name = 'Test Namee'
    }
    parameters  {
        string(name:"person",description:"person name", defaultValue:"Ali")
        booleanParam(name:"Test",description:"Test",defaultValue:true)
        booleanParam(name:"Build",description:"Build",defaultValue:true)
        booleanParam(name:"Deploy",description:"Deploy",defaultValue:true)
    }
    stages {
        stage('Test') {
            steps {
                echo "Testing variable = ${name}"
                echo 'Testing'
            }
        }
        stage('Build') {
            environment {
                testName = 'Test Name2'
            }
            steps {
                echo "Building = ${testName}"
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
