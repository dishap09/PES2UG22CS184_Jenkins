pipeline {
    agent any 
    stages {
        
        stage('Build') {
            steps {
                build 'PES2UG22CS184-1'
                sh 'g++ main/main.cpp -o output'
            }
        }

        stage('Test') {
            steps { 
                sh './output'
            }
        }

        stage('Deploy') { 
            steps { 
                echo 'Deployed' 
            } 
        } 

    } 

    post { 
        failure { 
            error 'Pipeline failed' 
        }  
    }  
}
