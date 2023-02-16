pipeline {
    agent any
    stages {
        stage('Echo'){
        steps {
                sh "echo 'step 1'"
            } 
        }
        stage('ls'){
            steps {
              sh "ls -a"
            }
        }
        stage('pwd'){
            steps {
              sh "pwd"
            }
        }
        stage('touch file'){
            steps {
              sh "touch file"
            }
        }
        stage('move it'){
            steps {
              sh '''
                mkdir movedIt
                mv file movedIt
              '''
            }
        }
    }
}
