pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                echo "Deploying all files and directories via Jenkins..."
                sh '''
                  rsync -av --progress --delete --exclude .git/ ./ faiza@192.168.56.105:/var/www/html/
             
                '''
            }
        }
    }
}

