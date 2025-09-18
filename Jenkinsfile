pipeline {
    agent any

    stages {
        
        

        stage('Deploy') {
            steps {
                echo "Deploying only welcome.html via Jenkins..."
          rsync -av --progress --exclude .git/ ./ faiza@192.168.56.105:/var/www/html/


            }
        }
    }
}
