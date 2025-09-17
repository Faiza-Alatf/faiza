pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    credentialsId: 'git-ssh-key',
                    url: 'git@github.com:Faiza-Alatf/faiza.git'
            }
        }

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

