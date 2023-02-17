pipeline {
    agent any
    stages {
        stage('Build app'){
        steps {
                sh "docker build -t jackqa/task3-app ./app"
            } 
        }
        stage('Build proxy'){
            steps {
              sh "docker build -t jackqa/task3-proxy ./proxy"
            }
        }
        stage('Create net'){
            steps {
              sh "docker network create webapp"
            }
        }        
        stage('Start app'){
            steps {
              sh "docker run --name webapp --net webapp -dit jackqa/task3-app"
            }
        }
        stage('Start proxy'){
            steps {
              sh "docker run --name proxy -p 80:80 --net webapp -dit jackqa/task3-proxy"
            }
        }
    }
}

