pipeline {

    agent any

    stages {

        stage ("Cleanup Workspace") {
            steps {
                cleanWs()
            }   
        }

        stage ("Checkout From SCM") {
            steps {
            git branch: 'main', credentialsId: 'marviflame', url: 'https://github.com/marviflame/OctoberProject.git'
            }   
        }

        stage ("Build Application") {
            steps {
                sh 'mvn clean install'
            }   
        }
        
       stage ("Test Application") {
            steps {
                sh 'mvn test'
            }   
        }

        stage ("Sonarqube Analysis") {
            steps {
                script {
                     withSonarQubeEnv(credentialsId: 'sonar_token') {
                      sh 'mvn sonar:sonar'  
                    }
                }    
            }
        }    

    }
}
