pipeline {
    agent any

    stages {
        stage('Loading Pipeline') {
            steps {
                script {
                load "$WORKSPACE/myfile.groovy"
                echo "${env.test}"
                def test = "${env.test}"
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
              
                environment name: ''${test}'', value: 'test' 
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
