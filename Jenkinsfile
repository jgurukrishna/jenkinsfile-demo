pipeline{
    tools{
        maven 'myMaven'
    }
    agent any
    stages{
        stage('Clone repo'){
            steps{
                git 'https://github.com/jgurukrishna/DevOpsClassCodes.git'
            }
        }
        stage('compile'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('Code review'){
            steps{
                sh 'mvn pmd:pmd'
            }
        }
        stage('Test code'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package'){
            steps{
                sh 'mvn package'
            }
        }
        
    }
    
}
