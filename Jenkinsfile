pipeline {
    agent any
    stages {
        stage('Building'){
            environment {
                HOME="."
            }
            steps{
                bat 'pip install -r requirements.txt'
            }
        }
        stage('Testing'){
            steps{
                bat 'python -m unittest'
            }
        }
        stage('Deploying'){
            steps{
                bat 'docker build -t faskimage .'
                bat 'docker run -d -p 8000:8000 --name faskcontainer faskimage'
            }
        }
    }
}