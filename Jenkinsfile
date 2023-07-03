pipeline {
    agent any
    stages {
        stage('git checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/hadilahmed05/demo-app.git'
            }
        }
        stage('unit testing') {
            steps {
                sh 'mvn test'
            }
        }
        stage('maven version'){
            
            steps{
                
                script{
                    
                    sh 'mvn --version'
                }
            }
        }
        stage('Integration testing'){
            
            steps{
                
                script{
                    tool 'Maven3.6.3'
                    
                    sh 'mvn verify'
                }
            }
        }
    }
}