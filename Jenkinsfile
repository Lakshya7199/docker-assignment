pipeline{
    agent any
    stages{
        stage("Clean Up"){
            steps {
                deleteDir()
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
