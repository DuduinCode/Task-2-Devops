pipeline{
    agent any;
    
    stages{
        stage("Code CLone"){
            steps{
                git url:"https://github.com/LondheShubham153/node-todo-cicd.git", branch:"master"
            }
        }
        stage("Image build & Test"){
            steps{
                sh "docker build -t node-app ."
            }
        }
        stage("Deploy"){
            steps{
                sh "docker compose up -d"
            }
        }
            
        }
    }
