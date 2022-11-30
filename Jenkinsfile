pipeline {
    agent {label "nginx_tst1"}
    stages {
        stage("Checkout") {
            steps {
                git 'https://github.com/andy-dkit/devops-ex1.git'
                echo "Stage 1- Checkout"
                sh "pwd"
            }
        }
        stage("Copy Files to Nginx") {
            steps {
                sh "cp -r * /usr/share/nginx/html"
            }
        }       
    }
}
