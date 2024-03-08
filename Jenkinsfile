pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                build 'PES2UG21CS344-1'
                sh "g++ PES2UG21CS344-1.cpp -o output"
            }
        }
        stage('Test') {
            steps {
                sh "./output"
            }
        }
        stage('Deploy') { 
            steps { 
                echo 'deploy' 
            } 
        }   
    }   
    post {  
         failure {  
             error "Pipeline failed"  
         }  
     }   
}
