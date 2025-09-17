pipeline {
    agent any

    stages {
       

        stage('Deploy') {
            steps {
                sh '''
                    echo "Deploying files via Jenkins..."
                    cp -r * /var/www/html/
                '''
            }
        }
    }
}

