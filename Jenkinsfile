pipeline {
  agent any

  stages {
    stage('Source Code Management Checkout')
      steps {
         // Clone your repository
         git branch: 'master'
            url: 'https://github.com/muahmed471/simple_php_application.git'
      }
    }
    
    stage('Compile') {
      steps {
          sh 'sudo yum install httpd php php-mysql php-fpm -y'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying application...'
        // Example command
          sh ' sudo systemctl restart httpd'
      }
    }

    post {
      success {
        echo 'Pipeline completed successfully'
      }
      failure {
        echo 'Pipeline failed'
      }
  }
}          
