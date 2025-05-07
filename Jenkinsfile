pipeline{
    agent any
    environment {
        DB_USER = 'user'
        DB_PASSWORD = 'password'
    }

    stages{
        stage("Checkout"){
            steps{
                script{
                    git branch: 'main', url: 'https://github.com/nithin282004/etp.git'
                }
            }
        }
        stage("Build"){
            steps{
                script{
                    sh 'docker-compose up'
                }

            }
        }
    }
        
    post{   
        success{
            echo "success"
        }
        failure{
            echo "failure"
        }
    }
}
