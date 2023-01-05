pipeline {
    agent any
    stages {
        stage('Building'){
            steps{
                bat 'pip install --target ${env.WORKSPACE} -r requirements.txt'
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