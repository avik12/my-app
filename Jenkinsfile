pipeline{
    agent any 
    tools {
        maven 'Maven1'
    }    
        stages {
            stage("git Checkout"){
                steps{
                     git 'https://github.com/avik12/my-app.git'  
                }
            }
            stage("maven Build"){
                steps{
                     sh 'mvn clean package'   
                }
            }
            stage("slack Message"){
            slackSend baseUrl: 'https://hooks.slack.com/services/', channel: '#jenkins-demo-123', color: 'good', message: 'Welcome To Slack Jenkins', teamDomain: 'app.slack.com', tokenCredentialId: 'Jenkins-slack-demo'
            } 
        }
    }
