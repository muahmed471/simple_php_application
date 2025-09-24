pipeline {
    agent any

    stages {
        stage('Source Code Management Checkout') {
            steps {
                git branch: 'master',
                    url: 'https://github.com/muahmed471/simple_php_application.git'
            }
        }

        stage('Compile') {
            steps {
                echo 'Compiling the application...'
                // For PHP you might not really "compile", but run a syntax check
                sh 'php -l index.php'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Example: copy to Apache/Nginx root
                sh 'cp -r * /var/www/html/'
            }
        }
    }
}
