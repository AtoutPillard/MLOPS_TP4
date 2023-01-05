pipeline {
    agent any
    stage{
        stage('Building'){
            steps{
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Building'){
            steps{
                sh 'python -m unittest'
            }
        }
    }
}