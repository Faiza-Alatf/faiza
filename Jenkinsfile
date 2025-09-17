pipeline {
    agent any

    stages {
       

        stage('Deploy') {
            steps {
                sh '''
                    echo "Deploying files via Jenkins..."
                   rsync -av --progress ${WORKSPACE} /var/www/welcome/

                '''
            }
        }
    }
}

