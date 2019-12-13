pipeline {
    agent {label 'master'}
    stages {
        stage('Build'){
            steps {
                echo 'Buiding...'   
            }
        }
        stage('Test'){
            steps{
               echo 'Testing...' 
               input "Does the staging environment look ok?" 
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deploying...'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}