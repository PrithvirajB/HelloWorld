pipeline {
    agent any
    
    tools{
        maven 'Maven'
    }
    parameters {
        choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }
    stages {
        stage('build') {
            steps{
                sh 'mvn clean install'
                echo 'building...'
            }
        }
        stage('test') {
	     when {
                expression {
                    params.executeTests
                }
            }
            steps{
                echo 'testing...'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying...'
		echo 'deploying... ${params.VERSION}'
            }
        }
    }
}
