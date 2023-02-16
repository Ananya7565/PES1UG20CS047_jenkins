
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -c hello.cpp' 
                sh 'g++ -o hello hello.cpp'
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
