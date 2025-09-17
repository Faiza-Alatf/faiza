pipeline {
    agent any

    stages {
       

        stage('Deploy') {
            steps {
                sh '''
                    echo "Deploying files via Jenkins..."
                   sudo cp -r index.html welcome.html /var/www/html/
                '''
            }
        }
    }
}

