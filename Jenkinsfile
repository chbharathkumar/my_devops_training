pipeline {
    agent any

    stages {
        stage('Loading Pipeline') {
            steps {
                script {
                load "$WORKSPACE/myfile.groovy"
                def build = "${env.build}"
                def test = "${env.test}"
                def deploy = "${env.deploy}"
                }
            }
        }
        stage('Build') {
            when {
              
              expression { env.build == 'yes' }
             }
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            when {
              
              expression { env.test == 'yes' }
             }
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            when {
              
              expression { env.deploy == 'yes' }
             }
            steps {
                echo 'Deploying....'
            }
        }
    }
}
