pipeline {
    agent any

    tools {
        maven 'Maven 3'
    }

    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Run tests or not')
    }

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
            when {
                expression { params.executeTests }
            }
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
}pipeline {
    agent any

    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Run tests or not')
    }

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
            when {
                expression { params.executeTests }
            }
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
