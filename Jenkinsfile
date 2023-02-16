
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -c hello.cpp' 
                sh 'g++ -o hello hello.cpp'
                sh 'Build successful'
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
/*
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o hello hello.cpp'
            }
        }

        stage('Test') {
            steps {
                sh './hello'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deployed successfully'
            }
        }
    }

    post {
        always {
            script {
                if (currentBuild.result == 'FAILURE') {
                    echo 'pipeline failed'
                }
            }
        }
    }
}
*/
