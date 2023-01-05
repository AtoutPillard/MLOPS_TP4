pipeline {
    agent any
    stages {
        stage('Building'){
            steps{
                bat 'python -m pip install -r requirements.txt'
            }
        }
        stage('Testing'){
            steps{
                bat 'python -m unittest'
            }
        }
    }
}