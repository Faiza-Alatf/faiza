pipeline {
    agent any

    stages {
       

        stage('Deploy') {
            steps {
                sh '''
                    echo "Deploying files via Jenkins..."
                   rsync -av --progress ${WORKSPACE} faiza@192.168.56.105:/var/www/welcome/

                '''
            }
        }
    }
}

