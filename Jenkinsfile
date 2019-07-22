

pipeline {
    
    agent any
    
    stages{
        
        stage('Clone repo and clean it'){
            
            steps{
                sh "rm -rf my-app"
                sh "git clone https://github.com/ozaytunctan/spring-boot-rest-service-crud.git"
                sh "mvn clean -f my-app"
                echo "Clone repo and clean it"
            }
            
        }
        
        
        stage('TEST'){

            steps{
                sh "mvn test -f my-app"
               echo "TEST running successfully"
            }
            
        }
            stage('DEPLOY'){
            steps{
                sh "mvn package -f my-app"
                echo "Deploy running successfully"
            }
            
        }
        }
}
