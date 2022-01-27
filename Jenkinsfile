pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
    
  post {
        // If Maven was able to run the tests, even if some of the test
        // failed, record the test results and archive the jar file.
        failure {
            always
            {
                emailext body: 'Summary', subject: 'Jenkin Build Failure', to: 'usmansharif994@gmail.com'
            }
        }
    }
}
