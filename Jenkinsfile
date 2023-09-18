
pipeline{
    agent any
    stages {
        stage('to get the code'){
            steps{
                git branch: 'ansible-sonar', url: 'https://github.com/suhasabn/java.git'
            }
        }
        stage('code-compile'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('code-test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('code-qa'){
            steps{
                sh 'mvn pmd:pmd'
            }
        }
        stage('code-package'){
            steps{
                sh 'mvn package'
            }
        }
    }
}
