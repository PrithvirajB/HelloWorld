pipeline {
    agent any
    
    tools{
        maven 'Maven'
    }
    
    stages {
        stage('build') {
            steps{
                sh 'mvn clean install'
                echo 'building...'
            }
        }
        stage('test') {
            steps{
                echo 'testing...'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying...'
            }
        }
    }
}