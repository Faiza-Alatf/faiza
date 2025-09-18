pipeline {
    agent any

    stages {
        
        

        stage('Deploy') {
            steps {
                echo "Deploying only welcome.html via Jenkins..."
             sh 'rsync -av --progress --exclude .git/ welcome.html faiza@192.168.56.105:/var/www/html/'


            }
        }
    }
}
