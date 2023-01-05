pipeline {
    agent any
    stages {
        stage('Building'){
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
                bat 'docker build -t flaskimage .'
                bat 'docker run -d -p 8000:8000 flaskimage'
            }
        }
    }
}
