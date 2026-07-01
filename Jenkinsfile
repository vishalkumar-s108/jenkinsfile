pipeline {
    agent any 

    environment {
        // Jenkins locker se secret nikal kar is variable mein daal rahe hain
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
                
                // Hum jaanbujhkar password ko print karne ki koshish kar rahe hain
                sh "echo 'This is my password: ${DB_PASSWORD}'"
            }
        }
    }
}
