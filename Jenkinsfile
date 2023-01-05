pipeline {
    agent any
    stages {
        stage('Building'){
            environment {
                HOME="."
            }
            steps{
                bat 'pip3 install -r requirements.txt'
            }
        }
        stage('Testing'){
            steps{
                bat 'python3 -m unittest'
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