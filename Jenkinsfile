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
        stage('Start app'){
            steps {
              sh "docker run -dit jackqa/task3-app webapp"
            }
        }
        stage('Start proxy'){
            steps {
              sh "docker run -dit jackqa/task3-proxy proxy"
            }
        }
    }
}
