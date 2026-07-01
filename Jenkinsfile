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
                echo 'Chalo check karte hain ki password dikh raha hai ya nahi...'
                
                // Hum jaanbujhkar password ko print karne ki koshish kar rahe hain
                sh "echo 'Mera password ye hai: ${DB_PASSWORD}'"
            }
        }
    }
}
