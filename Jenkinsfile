pipeline{
    agent any
    stages{
        stage("Clean Up"){
            steps {
                deleteDir()
            }
        }
        stage("Checkout Code") {
            steps {
        sh "git clone https://github.com/Lakshya7199/docker-assignment.git"
            }
        }

        stage("Build"){
            steps{
                dir("docker-assignment/backend"){
                    
                    sh "docker build -t backend . "
                    
                }
                dir("docker-assignment/frontend"){
                    
                    sh "docker build -t frontend . "
                    
                }
                dir("docker-assignment"){
                    
                    sh "docker-compose up --build "
                    
                }                
            }
        }

    }
}
