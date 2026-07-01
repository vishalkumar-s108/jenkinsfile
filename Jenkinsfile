pipeline {
    agent any 

    environment {
       
        DB_PASSWORD = credentials('my-db-pass')
    }

    stages {
        stage('Welcome') {
            steps {
                echo 'Securing our pipeline...'
            }
        }
        stage('Test Secret Masking') {
            steps {
                echo 'Lets go check your password...'
                
            
                sh "echo 'This is my password: ${DB_PASSWORD}'"
            }
        }
    }
}
