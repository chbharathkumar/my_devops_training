pipeline {
    agent any

    stages {
        stage('Loading Pipeline') {
            steps {
                script {
                load "$WORKSPACE/myfile.groovy"
                echo "${env.test}"
                }
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            when {
              
              environment name: 'env.test', value: 'test' 
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
}
