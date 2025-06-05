pipeline {
    agent any
    
    stages{
        stage("Code"){
            steps{
                git url: "https://github.com/SameerG16/Two-tier-flask-app.git", branch: "main"
            }
        }
        stage("Build & Test"){
            steps{
                sh "docker build . -t flaskapp"
            }
        }
        stage("Deploy"){
            steps{
                sh "docker-compose down && docker-compose up -d"
            }
        }
    }
}
