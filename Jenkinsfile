pipeline {
    agent any

    environment {
        MY_VAR = "HelloFromEnv"
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                echo "${MY_VAR}"
            }
        }

        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished'
        }
    }
}
