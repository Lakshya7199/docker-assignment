pipeline{
    agent any
    stages{
        stage("Clean Up"){
            steps {
                deleteDir()
            }
        }
        stage("clone repo"){
            steps {
                sh "git clone https://github.com/Lakshya7199/docker-assignment.git"
            }
        }
        stage("Build"){
            steps{
                dir("docker-assignment/backend"){
                    
                    sh "docker build -t back . "
                    
                }
                dir("docker-assignment/frontend"){
                    
                    sh "docker build -t front . "
                    
                }
                dir("docker-assignment"){
                    
                    sh "docker-compose up --build "
                    
                }                
            }
        }

    }
}
