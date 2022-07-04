pipeline{
    agent any {
    tools {
        maven 'Maven1'
    }    
        stages {
            stage("git Checkout"){
                steps{
                     sh 'git 'https://github.com/avik12/my-app.git'   
                }
            }
            stage("maven Build"){
                steps{
                     sh 'mvn clean package'   
                }
            }    
            }
        }
    }
}
