pipeline {
    agent any

    environment {
        USERNAME = "faiza"
        SERVER = "192.168.56.105"
        DEPLOY_PATH = "/var/www/html/maham/"
    }

    stages {
        stage('Deploy to Apache') {
            steps {
                sh """
                    rsync -av --delete --exclude ".git/" --exclude "Jenkinsfile" ${WORKSPACE}/ ${USERNAME}@${SERVER}:${DEPLOY_PATH}/
                    ssh ${USERNAME}@${SERVER} "sudo systemctl restart apache2"
                """
            }
        }
    }
}

