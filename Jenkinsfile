pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ temp.cpp -o temp'
                 build job: 'PES1UG20CS501-1', wait: false
                 echo 'Build by CS509 successful'
            }
        }

        stage('Test') {
            steps {
                sh 'cat temp.cpp'
                echo 'Test by CS509 successful'
            }
        }

        stage('Deploy') {
            steps {
               
                echo 'Deploy by CS509 successful'
            }
        }
    }

    post {
        failure {
            
                echo 'Pipeline Failed'
          
        }
    }
}
