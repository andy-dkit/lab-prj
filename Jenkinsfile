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
                sh "cp -r *.html /usr/share/nginx/html"
                sh "cp -r images /usr/share/nginx/html/images"
            }
        }
        stage("Start Python server") {
            steps {
                echo "Starting Server"
                sh "cd server"
                sh "python server.py"
            }
        }   
    }
}
