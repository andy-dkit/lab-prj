pipeline {
    agent none
    stages {
        stage("Checkout") {
            agent {label "nginx_tst1"}
            steps {
                git 'https://github.com/andy-dkit/devops-ex1.git'
                echo "Stage 1- Checkout"
                sh "pwd"
            }
        }
        stage("Copy Files to Nginx") {
            agent {label "python_tst1"}
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
