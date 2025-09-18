pipeline {
    agent any

    stages {
        stage('Checkout welcome.html only') {
            steps {
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/main']],
                    extensions: [
                        [$class: 'SparseCheckoutPaths',
                         sparseCheckoutPaths: [[path: 'welcome.html']]]
                    ],
                    userRemoteConfigs: [[url: 'git@github.com:Faiza-Alatf/faiza.git']]
                ])
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying only welcome.html via Jenkins..."
             sh 'rsync -av --progress --exclude ".git/" welcome.html faiza@192.168.56.105:/var/www/welcome/'

            }
        }
    }
}
