
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -c main/hello.cpp' 
                sh 'g++ -o hello main/hello.cpp'
                echo 'Build successful'
            }
        }
        stage('Test') {
            steps {
                sh './hello' 
                echo 'test stage executed successfully'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment successful'
                }
            }
}
  post{
    failure {
      echo 'Pipeline failure'
    }
  }
}
