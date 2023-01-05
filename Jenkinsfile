pipeline {
    agent any
    stages {
        stage('Building'){
            steps{
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Testing'){
            steps{
                sh 'python -m unittest'
            }
        }
    }
}